import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.io.InputStreamReader;

import java.util.*;

class Result {
    
    public static int[] complete_words( String words[], int scores[], String queries[] ) {
        
        int result[] = new int[ queries.length ];
        HashMap<String, Integer> checker = new HashMap<>();
        
        for( int i = 0; i < queries.length; i ++ ){
            checker.put( queries[i], -1 );
        }
        
        for( int i = 0; i < queries.length; i ++ ){
            
            for( int j = 0; j < words.length; j ++ ){
                
                if( words[j].startsWith( queries[i] ) ){
                    checker.put( queries[i], ( scores[j] > checker.get( queries[i] ) ) ? scores[j] : checker.get( queries[i] ) );
                    
                }
            }
            
        }
        
        for( int i = 0; i < queries.length; i ++ ){
            result[i] = checker.get( queries[i] );
        }
        
        return result;
        
    }
}
