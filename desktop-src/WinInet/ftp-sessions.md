---
title: Sesiones FTP
description: WinINet permite a las aplicaciones navegar y manipular directorios y archivos en un servidor FTP. Dado que los proxies de CERN no admiten FTP, las aplicaciones que usan exclusivamente el proxy CERN deben usar la función InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078047"
---
# <a name="ftp-sessions"></a><span data-ttu-id="193d5-104">Sesiones FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-104">FTP Sessions</span></span>

<span data-ttu-id="193d5-105">WinINet permite a las aplicaciones navegar y manipular directorios y archivos en un servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="193d5-106">Dado que los proxies de CERN no admiten FTP, las aplicaciones que usan exclusivamente el proxy CERN deben usar la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="193d5-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="193d5-107">Para obtener más información sobre cómo usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), consulte [acceso directo a las direcciones URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="193d5-108">Para iniciar una sesión de FTP, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para crear el identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="193d5-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="193d5-109">WinINet le permite realizar las siguientes acciones en un servidor FTP:</span><span class="sxs-lookup"><span data-stu-id="193d5-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="193d5-110">Desplazarse por los directorios.</span><span class="sxs-lookup"><span data-stu-id="193d5-110">Navigate between directories.</span></span>
-   <span data-ttu-id="193d5-111">Enumerar, crear, quitar y cambiar el nombre de los directorios.</span><span class="sxs-lookup"><span data-stu-id="193d5-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="193d5-112">Cambiar el nombre, cargar, descargar y eliminar archivos.</span><span class="sxs-lookup"><span data-stu-id="193d5-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="193d5-113">La navegación la proporcionan las funciones [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) y [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="193d5-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="193d5-114">Estas funciones usan el identificador de sesión creado por una llamada anterior a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para determinar el directorio en el que se encuentra la aplicación actualmente, o para cambiar a otro subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="193d5-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="193d5-115">La enumeración de directorios se realiza mediante las funciones [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) y [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="193d5-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="193d5-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para buscar el primer archivo que coincide con los criterios de búsqueda especificados y devuelve un identificador para continuar con la enumeración de directorios.</span><span class="sxs-lookup"><span data-stu-id="193d5-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="193d5-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usa el identificador devuelto por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) para devolver el siguiente archivo que coincide con los criterios de búsqueda originales.</span><span class="sxs-lookup"><span data-stu-id="193d5-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="193d5-118">La aplicación debe seguir llamando a [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) hasta que no queden más archivos en el directorio.</span><span class="sxs-lookup"><span data-stu-id="193d5-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="193d5-119">Utilice la función [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) para crear nuevos directorios.</span><span class="sxs-lookup"><span data-stu-id="193d5-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="193d5-120">Esta función usa el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y crea el directorio especificado por la cadena que se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="193d5-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="193d5-121">La cadena puede contener un nombre de directorio relativo al directorio actual o una ruta de acceso de directorio completa.</span><span class="sxs-lookup"><span data-stu-id="193d5-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="193d5-122">Para cambiar el nombre de los archivos o directorios, la aplicación puede llamar a [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="193d5-123">Esta función reemplaza el nombre original por el nuevo nombre que se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="193d5-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="193d5-124">El nombre del archivo o directorio puede ser relativo al directorio actual o a un nombre completo.</span><span class="sxs-lookup"><span data-stu-id="193d5-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="193d5-125">Para cargar o colocar archivos en un servidor FTP, la aplicación puede usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (junto con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span><span class="sxs-lookup"><span data-stu-id="193d5-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="193d5-126">Se puede usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) si el archivo ya existe localmente, mientras que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) se pueden usar si los datos se deben escribir en un archivo en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="193d5-127">Para descargar u obtener archivos, la aplicación puede usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) o [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span><span class="sxs-lookup"><span data-stu-id="193d5-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="193d5-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) se usa para recuperar un archivo de un servidor FTP y almacenarlo de forma local, mientras que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) se pueden usar para controlar dónde va la información descargada (por ejemplo, la aplicación podría mostrar la información en un cuadro de edición).</span><span class="sxs-lookup"><span data-stu-id="193d5-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="193d5-129">Elimine archivos en un servidor FTP mediante la función [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="193d5-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="193d5-130">Esta función quita un nombre de archivo que es relativo al directorio actual o a un nombre de archivo completo del servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="193d5-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requiere un identificador de sesión devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="193d5-132">Controladores de funciones FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-132">FTP Function Handles</span></span>

<span data-ttu-id="193d5-133">Para que funcione correctamente, las funciones de FTP requieren determinados tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="193d5-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="193d5-134">Estos identificadores deben crearse en un orden específico, empezando por el identificador raíz creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="193d5-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="193d5-135">A continuación, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) puede crear un identificador de sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="193d5-136">En el diagrama siguiente se muestran las funciones que dependen del identificador de sesión FTP devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="193d5-137">Los cuadros sombreados representan funciones que devuelven los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , mientras que los cuadros simples representan funciones que utilizan el identificador HINTERNET creado por la función de la que dependen.</span><span class="sxs-lookup"><span data-stu-id="193d5-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![funciones FTP que dependen del identificador de sesión FTP devuelto por internetconnect](images/ax-wnt06.png)

<span data-ttu-id="193d5-139">En el diagrama siguiente se muestran las dos funciones que devuelven los identificadores [HINTERNET](appendix-a-hinternet-handles.md) y las funciones que dependen de ellos.</span><span class="sxs-lookup"><span data-stu-id="193d5-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="193d5-140">Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.</span><span class="sxs-lookup"><span data-stu-id="193d5-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![funciones de FTP que devuelven identificadores de HINTERNET](images/ax-wnt03.png)

<span data-ttu-id="193d5-142">Para obtener más información, vea [identificadores de HINTERNET](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="193d5-143">Usar las funciones WinINet para sesiones FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="193d5-144">Las siguientes funciones se usan durante las sesiones FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="193d5-145">Los proxies de CERN no reconocen estas funciones.</span><span class="sxs-lookup"><span data-stu-id="193d5-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="193d5-146">Las aplicaciones que deben funcionar a través de servidores proxy CERN deben usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y tener acceso directamente a los recursos.</span><span class="sxs-lookup"><span data-stu-id="193d5-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="193d5-147">Para obtener más información sobre el acceso directo a los recursos, consulte [acceso directo a las direcciones URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="193d5-148">Función</span><span class="sxs-lookup"><span data-stu-id="193d5-148">Function</span></span>                                                 | <span data-ttu-id="193d5-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="193d5-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="193d5-150">**FtpCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="193d5-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="193d5-151">Crea un nuevo directorio en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-151">Creates a new directory on the server.</span></span> <span data-ttu-id="193d5-152">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="193d5-153">**FtpDeleteFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="193d5-154">Elimina un archivo del servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-154">Deletes a file from the server.</span></span> <span data-ttu-id="193d5-155">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="193d5-156">**FtpFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="193d5-157">Inicia la enumeración de archivos o la búsqueda de archivos en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="193d5-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="193d5-158">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="193d5-159">**FtpGetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="193d5-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="193d5-160">Devuelve el directorio actual del cliente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="193d5-161">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="193d5-162">**FtpGetFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="193d5-163">Recupera un archivo del servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-163">Retrieves a file from the server.</span></span> <span data-ttu-id="193d5-164">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="193d5-165">**FtpOpenFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="193d5-166">Inicia el acceso a un archivo en el servidor para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="193d5-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="193d5-167">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="193d5-168">**FtpPutFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="193d5-169">Escribe un archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-169">Writes a file to the server.</span></span> <span data-ttu-id="193d5-170">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="193d5-171">**FtpRemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="193d5-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="193d5-172">Elimina un directorio del servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-172">Deletes a directory on the server.</span></span> <span data-ttu-id="193d5-173">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="193d5-174">**FtpRenameFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="193d5-175">Cambia el nombre de un archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-175">Renames a file on the server.</span></span> <span data-ttu-id="193d5-176">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="193d5-177">**FtpSetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="193d5-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="193d5-178">Cambia el directorio actual del cliente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="193d5-179">Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="193d5-180">**InternetWriteFile**</span><span class="sxs-lookup"><span data-stu-id="193d5-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="193d5-181">Escribe datos en un archivo abierto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="193d5-182">Esta función requiere un identificador creado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="193d5-183">Iniciar una sesión de FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-183">Starting an FTP Session</span></span>

<span data-ttu-id="193d5-184">La aplicación establece una sesión FTP mediante una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) en un identificador creado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="193d5-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="193d5-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) necesita el nombre del servidor, el número de puerto, el nombre de usuario, la contraseña y el tipo de servicio (que debe establecerse en servicio de Internet \_ \_ FTP).</span><span class="sxs-lookup"><span data-stu-id="193d5-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="193d5-186">En el caso de la semántica de FTP pasivo, la aplicación también debe establecer la marca [ \_ \_ pasiva de marca de Internet](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="193d5-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="193d5-187">El \_ puerto FTP predeterminado de Internet \_ \_ y \_ \_ \_ los valores de número de puerto de Internet no válidos se pueden usar para el número de puerto.</span><span class="sxs-lookup"><span data-stu-id="193d5-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="193d5-188">El \_ puerto FTP predeterminado de Internet \_ \_ utiliza el puerto FTP predeterminado, pero todavía debe establecerse el tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="193d5-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="193d5-189">El \_ \_ número de puerto de Internet no válido \_ usa el valor predeterminado para el tipo de servicio indicado.</span><span class="sxs-lookup"><span data-stu-id="193d5-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="193d5-190">Los valores de nombre de usuario y contraseña pueden establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="193d5-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="193d5-191">Si ambos valores están establecidos en **null**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa "Anonymous" para el nombre de usuario y la dirección de correo electrónico del usuario para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="193d5-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="193d5-192">Si solo la contraseña se establece en **null**, el nombre de usuario que se pasa a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) se usa para el nombre de usuario y se usa una cadena vacía para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="193d5-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="193d5-193">Si ninguno de los valores es **null**, se usan el nombre de usuario y la contraseña proporcionados a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="193d5-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="193d5-194">Enumerar directorios</span><span class="sxs-lookup"><span data-stu-id="193d5-194">Enumerating Directories</span></span>

<span data-ttu-id="193d5-195">La enumeración de un directorio en un servidor FTP requiere la creación de un controlador de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="193d5-196">Este identificador es una rama del identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="193d5-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) busca el primer archivo o directorio en el servidor y lo devuelve en una estructura [**de \_ \_ datos de búsqueda de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="193d5-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="193d5-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) hasta que devuelva el [**error \_ no \_ más \_ archivos**](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="193d5-199">Este método busca todos los archivos y directorios subsiguientes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="193d5-200">Para obtener más información sobre [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consulte [Buscar el siguiente archivo](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="193d5-201">Para determinar si el archivo recuperado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) es un directorio, compruebe el miembro **dwFileAttributes** de la estructura de [**\_ \_ datos de búsqueda de Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) para ver si es igual al directorio de atributos de archivo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="193d5-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="193d5-202">Si la aplicación realiza cambios en el servidor FTP o si el servidor FTP cambia con frecuencia, se deben establecer las marcas de [Internet Flag \_ \_ no \_ Cache \_ Write](api-flags.md) y [Internet \_ Flag \_ Reload](api-flags.md) en [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="193d5-203">Estas marcas garantizan que la información de directorio que se recupera del servidor FTP es actual.</span><span class="sxs-lookup"><span data-stu-id="193d5-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="193d5-204">Una vez que la aplicación completa la enumeración de directorios, la aplicación debe realizar una llamada a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) en el identificador creado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="193d5-205">Hasta que se cierre el identificador, la aplicación no podrá volver a llamar a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) en el identificador de sesión creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="193d5-206">Si se realiza una llamada a [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) en el mismo identificador de sesión antes de que se cierre la llamada anterior a la misma función, se produce un error en la función y se devuelve el [error \_ \_ de transferencia FTP \_ en \_ curso](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="193d5-207">En el ejemplo siguiente se enumera el contenido de un directorio FTP en un control de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="193d5-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="193d5-208">El parámetro *hConnection* es un identificador devuelto por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) después de que se establece una sesión FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="193d5-209">Puede encontrar el código fuente de ejemplo para la función InternetErrorOut a la que se hace referencia en este ejemplo en el tema [errores de control](appendix-c-handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="193d5-210">Navegar por los directorios</span><span class="sxs-lookup"><span data-stu-id="193d5-210">Navigating Directories</span></span>

<span data-ttu-id="193d5-211">Las funciones [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) y [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) controlan la navegación del directorio.</span><span class="sxs-lookup"><span data-stu-id="193d5-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="193d5-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) devuelve el directorio actual de la aplicación en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="193d5-213">Se incluye la ruta de acceso del directorio desde el directorio raíz del servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="193d5-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) cambia el directorio de trabajo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="193d5-215">La información del directorio que se pasa a [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) puede ser un nombre de ruta de acceso parcial o completo en relación con el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="193d5-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="193d5-216">Por ejemplo, si la aplicación se encuentra actualmente en el directorio "Public/info" y la ruta de acceso es "FTP/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) cambia el directorio actual a "Public/info/FTP/example".</span><span class="sxs-lookup"><span data-stu-id="193d5-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="193d5-217">En el ejemplo siguiente se usa el identificador de sesión FTP hConnection, devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="193d5-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="193d5-218">El nuevo nombre de directorio se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="193d5-219">Antes de realizar el cambio de directorio, la función recupera el directorio actual y lo almacena en el mismo cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="193d5-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="193d5-220">Aquí se muestra el código de código de código de la función DisplayFtpDir llamada al final.</span><span class="sxs-lookup"><span data-stu-id="193d5-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="193d5-221">Manipular directorios en un servidor FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="193d5-222">WinINet proporciona la capacidad de crear y quitar directorios en un servidor FTP en el que la aplicación tenga los privilegios necesarios.</span><span class="sxs-lookup"><span data-stu-id="193d5-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="193d5-223">Si la aplicación debe iniciar sesión en un servidor con un nombre de usuario y una contraseña específicos, los valores se pueden usar en [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) al crear el identificador de sesión FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="193d5-224">La función [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) toma un identificador de sesión FTP válido y una cadena terminada en **null** que contiene una ruta de acceso completa o un nombre relativo al directorio actual y crea un directorio en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="193d5-225">En el ejemplo siguiente se muestran dos llamadas independientes a [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span><span class="sxs-lookup"><span data-stu-id="193d5-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="193d5-226">En ambos ejemplos, hFtpSession es el identificador de sesión creado por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y el directorio raíz es el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="193d5-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="193d5-227">La función [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) toma un identificador de sesión y una cadena terminada en **null** que contiene una ruta de acceso completa o un nombre relativo al directorio actual y quita ese directorio del servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="193d5-228">En el ejemplo siguiente se muestran dos llamadas de ejemplo a [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span><span class="sxs-lookup"><span data-stu-id="193d5-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="193d5-229">En ambas llamadas, hFtpSession es el identificador de sesión creado por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y el directorio raíz es el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="193d5-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="193d5-230">Hay un directorio denominado "Test" en el directorio raíz y un directorio denominado "example" en el directorio "Test".</span><span class="sxs-lookup"><span data-stu-id="193d5-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="193d5-231">En el ejemplo siguiente se crea un nuevo directorio en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="193d5-232">El nuevo nombre de directorio se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="193d5-233">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="193d5-234">A continuación se muestra el código fuente de la función DisplayFtpDir llamada al final.</span><span class="sxs-lookup"><span data-stu-id="193d5-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="193d5-235">En el ejemplo siguiente se elimina un directorio del servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="193d5-236">El nombre del directorio que se va a eliminar se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa al parámetro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="193d5-237">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="193d5-238">A continuación se muestra el código fuente de la función DisplayFtpDir llamada al final.</span><span class="sxs-lookup"><span data-stu-id="193d5-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="193d5-239">Obtener archivos en un servidor FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="193d5-240">Existen tres métodos para recuperar archivos de un servidor FTP:</span><span class="sxs-lookup"><span data-stu-id="193d5-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="193d5-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="193d5-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="193d5-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="193d5-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="193d5-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="193d5-244">Para obtener más información sobre el uso de la función [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , vea [leer archivos](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="193d5-245">Si la dirección URL del archivo está disponible, la aplicación puede llamar a [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para conectarse a esa dirección URL y, a continuación, usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para controlar la descarga del archivo.</span><span class="sxs-lookup"><span data-stu-id="193d5-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="193d5-246">Esto permite que la aplicación tenga un mayor control sobre la descarga y es ideal para situaciones en las que no es necesario realizar ninguna otra operación en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="193d5-247">Para obtener más información sobre cómo acceder directamente a los recursos, consulte [acceso directo a las direcciones URL](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="193d5-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="193d5-248">Si la aplicación ha establecido un identificador de sesión FTP en el servidor con [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), la aplicación puede llamar a [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con el nombre de archivo existente y con un nuevo nombre para el archivo almacenado localmente.</span><span class="sxs-lookup"><span data-stu-id="193d5-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="193d5-249">A continuación, la aplicación puede utilizar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para descargar el archivo.</span><span class="sxs-lookup"><span data-stu-id="193d5-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="193d5-250">Esto permite que la aplicación controle mejor la descarga y mantiene la conexión con el servidor FTP, por lo que se pueden ejecutar más comandos.</span><span class="sxs-lookup"><span data-stu-id="193d5-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="193d5-251">Si la aplicación no necesita un control estricto sobre la descarga, la aplicación puede usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) con el identificador de sesión FTP, el nombre de archivo remoto y el nombre de archivo local para recuperar el archivo.</span><span class="sxs-lookup"><span data-stu-id="193d5-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="193d5-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) realiza toda la contabilidad y la sobrecarga asociada con la lectura de un archivo desde un servidor FTP y su almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="193d5-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="193d5-253">En el ejemplo siguiente se recupera un archivo de un servidor FTP y se guarda localmente.</span><span class="sxs-lookup"><span data-stu-id="193d5-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="193d5-254">El nombre del archivo en el servidor FTP se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nFtpFileNameId* y el nombre local en el que se guarda el archivo se toma del cuadro de edición, cuyo IDC se pasa en el parámetro *nLocalFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="193d5-255">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="193d5-256">Colocar archivos en un servidor FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="193d5-257">Hay dos métodos para colocar un archivo en un servidor FTP:</span><span class="sxs-lookup"><span data-stu-id="193d5-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="193d5-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) con [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span><span class="sxs-lookup"><span data-stu-id="193d5-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="193d5-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="193d5-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="193d5-260">Una aplicación que debe enviar datos a un servidor FTP, pero no tiene un archivo local que contenga todos los datos, debe utilizar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) para crear y abrir un archivo en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="193d5-261">A continuación, la aplicación puede utilizar [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para cargar la información en el archivo.</span><span class="sxs-lookup"><span data-stu-id="193d5-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="193d5-262">Si el archivo ya existe localmente, la aplicación puede utilizar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) para cargar el archivo en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="193d5-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) realiza toda la sobrecarga que se produce al cargar un archivo local en un servidor FTP remoto.</span><span class="sxs-lookup"><span data-stu-id="193d5-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="193d5-264">En el ejemplo siguiente se copia un archivo local en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="193d5-265">El nombre local del archivo se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nLocalFileNameId* y el nombre con el que se guarda el archivo en el servidor FTP se toma del cuadro de edición, cuyo IDC se pasa en el parámetro *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="193d5-266">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="193d5-267">Eliminar archivos de un servidor FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="193d5-268">Para eliminar un archivo de un servidor FTP, utilice la función [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="193d5-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="193d5-269">La aplicación que realiza la llamada debe tener los privilegios necesarios para eliminar un archivo del servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="193d5-270">En el ejemplo siguiente se elimina un archivo del servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="193d5-271">El nombre del archivo que se va a eliminar se toma del cuadro de edición del cuadro de diálogo primario, cuyo IDC se pasa int al parámetro *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="193d5-272">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="193d5-273">Puesto que esta función no actualiza los listados de archivos ni la presentación de directorios, el proceso de llamada debería hacerlo tras una eliminación correcta.</span><span class="sxs-lookup"><span data-stu-id="193d5-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="193d5-274">Cambiar el nombre de archivos y directorios en un servidor FTP</span><span class="sxs-lookup"><span data-stu-id="193d5-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="193d5-275">Se puede cambiar el nombre de los archivos y directorios de un servidor FTP mediante la función [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) .</span><span class="sxs-lookup"><span data-stu-id="193d5-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="193d5-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) acepta dos cadenas terminadas en **null** que contienen nombres parciales o completos en relación con el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="193d5-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="193d5-277">La función cambia el nombre del archivo designado por la primera cadena por el nombre designado por la segunda cadena.</span><span class="sxs-lookup"><span data-stu-id="193d5-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="193d5-278">En el ejemplo siguiente se cambia el nombre de un archivo o directorio en el servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="193d5-279">El nombre actual del archivo o directorio se toma del cuadro de edición del cuadro de diálogo principal cuyo IDC se pasa en el parámetro *nOldFileNameId* y el nuevo nombre se toma del cuadro de edición, cuyo IDC se pasa en el parámetro *nNewFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="193d5-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="193d5-280">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) creó el identificador de *hConnection* después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="193d5-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="193d5-281">Puesto que esta función no actualiza los listados de archivos ni la presentación de directorios, el proceso de llamada debería hacerlo tras cambiar el nombre correctamente.</span><span class="sxs-lookup"><span data-stu-id="193d5-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="193d5-282">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="193d5-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="193d5-283">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="193d5-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="193d5-284">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="193d5-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 