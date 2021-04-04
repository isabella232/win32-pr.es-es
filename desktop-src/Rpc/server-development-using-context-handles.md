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
# <a name="server-development-using-context-handles"></a><span data-ttu-id="1cf04-104">Desarrollo de servidores con identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="1cf04-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="1cf04-105">Desde la perspectiva del desarrollo de programas de servidor, un identificador de contexto es un puntero sin tipo.</span><span class="sxs-lookup"><span data-stu-id="1cf04-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="1cf04-106">Los programas de servidor inicializan los identificadores de contexto seleccionándolos en los datos de la memoria o en alguna otra forma de almacenamiento (como archivos en discos).</span><span class="sxs-lookup"><span data-stu-id="1cf04-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="1cf04-107">Por ejemplo, supongamos que un cliente utiliza un identificador de contexto para solicitar una serie de actualizaciones a un registro de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="1cf04-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="1cf04-108">El cliente llama a un procedimiento remoto en el servidor y le pasa una clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1cf04-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="1cf04-109">El programa de servidor busca la clave de búsqueda en la base de datos y obtiene el número de registro entero del registro coincidente.</span><span class="sxs-lookup"><span data-stu-id="1cf04-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="1cf04-110">A continuación, el servidor puede señalar un puntero a void en una ubicación de memoria que contiene el número de registro.</span><span class="sxs-lookup"><span data-stu-id="1cf04-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="1cf04-111">Cuando devuelve, el procedimiento remoto necesita devolver el puntero como un identificador de contexto a través de su valor devuelto o su lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="1cf04-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="1cf04-112">El cliente necesita pasar el puntero al servidor cada vez que llamó a procedimientos remotos para actualizar el registro.</span><span class="sxs-lookup"><span data-stu-id="1cf04-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="1cf04-113">Durante cada una de estas operaciones de actualización, el servidor convierta el puntero void en un puntero a un entero.</span><span class="sxs-lookup"><span data-stu-id="1cf04-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="1cf04-114">Una vez que el programa de servidor señala el identificador de contexto en los datos de contexto, se considera que el identificador está abierto.</span><span class="sxs-lookup"><span data-stu-id="1cf04-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="1cf04-115">Los identificadores que contienen un valor **null** están cerrados.</span><span class="sxs-lookup"><span data-stu-id="1cf04-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="1cf04-116">El servidor mantiene un identificador de contexto abierto hasta que el cliente llama a un procedimiento remoto que lo cierra.</span><span class="sxs-lookup"><span data-stu-id="1cf04-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="1cf04-117">Si la sesión de cliente finaliza mientras el identificador está abierto, el tiempo de ejecución de RPC llama a la rutina de ejecución del servidor para liberar el identificador.</span><span class="sxs-lookup"><span data-stu-id="1cf04-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="1cf04-118">En el fragmento de código siguiente se muestra cómo un servidor podría implementar un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="1cf04-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="1cf04-119">En este ejemplo, el servidor mantiene un archivo de datos que el cliente escribe en con procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="1cf04-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="1cf04-120">La información de contexto es un identificador de archivo que realiza un seguimiento de la ubicación actual en el archivo donde el servidor escribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="1cf04-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="1cf04-121">El identificador de archivo se empaqueta como un identificador de contexto en la lista de parámetros para llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="1cf04-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="1cf04-122">Una estructura contiene el nombre de archivo y el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="1cf04-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="1cf04-123">La definición de interfaz para este ejemplo se muestra en desarrollo de la [interfaz mediante identificadores de contexto](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="1cf04-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="1cf04-124">La función RemoteOpen abre un archivo en el servidor:</span><span class="sxs-lookup"><span data-stu-id="1cf04-124">The function RemoteOpen opens a file on the server:</span></span>


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



<span data-ttu-id="1cf04-125">La función RemoteRead Lee un archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1cf04-125">The function RemoteRead reads a file on the server.</span></span>


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



<span data-ttu-id="1cf04-126">La función RemoteClose cierra un archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1cf04-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="1cf04-127">Tenga en cuenta que la aplicación de servidor tiene que asignar **null** al identificador de contexto como parte de la función de cierre.</span><span class="sxs-lookup"><span data-stu-id="1cf04-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="1cf04-128">Esto se comunica con el código auxiliar del servidor y la biblioteca en tiempo de ejecución de RPC que se ha eliminado el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="1cf04-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="1cf04-129">De lo contrario, la conexión se mantendrá abierta y finalmente se producirá una ejecución de contexto.</span><span class="sxs-lookup"><span data-stu-id="1cf04-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


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
> <span data-ttu-id="1cf04-130">Aunque se espera que el cliente pase un identificador de contexto válido a una llamada con \[ in, \] atributos direccionales, RPC no rechaza identificadores de contexto **nulos** para esta combinación de atributos direccionales.</span><span class="sxs-lookup"><span data-stu-id="1cf04-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="1cf04-131">El identificador de contexto **null** se pasa al servidor como un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="1cf04-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="1cf04-132">El código de servidor para las llamadas que contienen un \[ identificador de contexto in, out \] debe escribirse para evitar una infracción de acceso cuando se recibe un puntero **null** .</span><span class="sxs-lookup"><span data-stu-id="1cf04-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




