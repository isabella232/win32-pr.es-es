---
title: Desarrollo de servidores con identificadores de contexto
description: Desde la perspectiva del desarrollo de programas de servidor, un identificador de contexto es un puntero sin tipo. Los programas de servidor inicializan los identificadores de contexto seleccionándolos en los datos de la memoria o en alguna otra forma de almacenamiento (como archivos en discos).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076166"
---
# <a name="server-development-using-context-handles"></a>Desarrollo de servidores con identificadores de contexto

Desde la perspectiva del desarrollo de programas de servidor, un identificador de contexto es un puntero sin tipo. Los programas de servidor inicializan los identificadores de contexto seleccionándolos en los datos de la memoria o en alguna otra forma de almacenamiento (como archivos en discos).

Por ejemplo, supongamos que un cliente utiliza un identificador de contexto para solicitar una serie de actualizaciones a un registro de una base de datos. El cliente llama a un procedimiento remoto en el servidor y le pasa una clave de búsqueda. El programa de servidor busca la clave de búsqueda en la base de datos y obtiene el número de registro entero del registro coincidente. A continuación, el servidor puede señalar un puntero a void en una ubicación de memoria que contiene el número de registro. Cuando devuelve, el procedimiento remoto necesita devolver el puntero como un identificador de contexto a través de su valor devuelto o su lista de parámetros. El cliente necesita pasar el puntero al servidor cada vez que llamó a procedimientos remotos para actualizar el registro. Durante cada una de estas operaciones de actualización, el servidor convierta el puntero void en un puntero a un entero.

Una vez que el programa de servidor señala el identificador de contexto en los datos de contexto, se considera que el identificador está abierto. Los identificadores que contienen un valor **null** están cerrados. El servidor mantiene un identificador de contexto abierto hasta que el cliente llama a un procedimiento remoto que lo cierra. Si la sesión de cliente finaliza mientras el identificador está abierto, el tiempo de ejecución de RPC llama a la rutina de ejecución del servidor para liberar el identificador.

En el fragmento de código siguiente se muestra cómo un servidor podría implementar un identificador de contexto. En este ejemplo, el servidor mantiene un archivo de datos que el cliente escribe en con procedimientos remotos. La información de contexto es un identificador de archivo que realiza un seguimiento de la ubicación actual en el archivo donde el servidor escribirá los datos. El identificador de archivo se empaqueta como un identificador de contexto en la lista de parámetros para llamadas a procedimientos remotos. Una estructura contiene el nombre de archivo y el identificador de archivo. La definición de interfaz para este ejemplo se muestra en desarrollo de la [interfaz mediante identificadores de contexto](interface-development-using-context-handles.md).


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



La función RemoteOpen abre un archivo en el servidor:


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



La función RemoteRead Lee un archivo en el servidor.


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



La función RemoteClose cierra un archivo en el servidor. Tenga en cuenta que la aplicación de servidor tiene que asignar **null** al identificador de contexto como parte de la función de cierre. Esto se comunica con el código auxiliar del servidor y la biblioteca en tiempo de ejecución de RPC que se ha eliminado el identificador de contexto. De lo contrario, la conexión se mantendrá abierta y finalmente se producirá una ejecución de contexto.


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> Aunque se espera que el cliente pase un identificador de contexto válido a una llamada con \[ in, \] atributos direccionales, RPC no rechaza identificadores de contexto **nulos** para esta combinación de atributos direccionales. El identificador de contexto **null** se pasa al servidor como un puntero **nulo** . El código de servidor para las llamadas que contienen un \[ identificador de contexto in, out \] debe escribirse para evitar una infracción de acceso cuando se recibe un puntero **null** .

 

 

 




