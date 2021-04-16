---
title: Funciones comunes (Internet de Windows)
description: Los diferentes protocolos de Internet (como FTP y http) usan varias de las mismas funciones de WinINet para controlar la información en Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714511"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="f1fdc-103">Funciones comunes (Internet de Windows)</span><span class="sxs-lookup"><span data-stu-id="f1fdc-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="f1fdc-104">Los diferentes protocolos de Internet (como FTP y http) usan varias de las mismas funciones de WinINet para controlar la información en Internet.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="f1fdc-105">Estas funciones comunes controlan sus tareas de forma coherente, independientemente del protocolo concreto al que se aplican.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="f1fdc-106">Las aplicaciones pueden usar estas funciones para crear funciones de uso general que controlan las tareas en los diferentes protocolos (como la lectura de archivos para FTP y http).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="f1fdc-107">Las funciones comunes de controlan las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1fdc-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="f1fdc-108">Descargar recursos de Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)y [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="f1fdc-109">Configurar operaciones asincrónicas ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="f1fdc-110">Ver y cambiar opciones ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="f1fdc-111">Cerrar todos los tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="f1fdc-112">Colocar y quitar bloqueos en los recursos ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) y [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="f1fdc-113">Usar funciones comunes</span><span class="sxs-lookup"><span data-stu-id="f1fdc-113">Using Common Functions</span></span>

<span data-ttu-id="f1fdc-114">En la tabla siguiente se enumeran las funciones comunes incluidas en las funciones de WinINet.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="f1fdc-115">Las funciones comunes se pueden usar en diferentes tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) o se pueden usar durante diferentes tipos de sesiones.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="f1fdc-116">Función</span><span class="sxs-lookup"><span data-stu-id="f1fdc-116">Function</span></span>                                                         | <span data-ttu-id="f1fdc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1fdc-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1fdc-118">**InternetFindNextFile**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="f1fdc-119">Continúa la enumeración o búsqueda de archivos.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-119">Continues file enumeration or search.</span></span> <span data-ttu-id="f1fdc-120">Requiere un identificador creado por la función [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="f1fdc-121">**InternetLockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="f1fdc-122">Permite al usuario colocar un bloqueo en el archivo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="f1fdc-123">Esta función requiere un identificador devuelto por la función [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="f1fdc-124">**InternetQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="f1fdc-125">Recupera la cantidad de datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="f1fdc-126">Requiere un identificador creado por la función [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="f1fdc-127">**InternetQueryOption**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="f1fdc-128">Recupera el valor de una opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="f1fdc-129">**InternetReadFile**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="f1fdc-130">Lee los datos de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-130">Reads URL data.</span></span> <span data-ttu-id="f1fdc-131">Requiere un identificador creado por la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="f1fdc-132">**InternetSetFilePointer**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="f1fdc-133">Establece la posición para la siguiente lectura en un archivo.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="f1fdc-134">Requiere un identificador creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo en una dirección URL http) o un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) mediante el verbo HTTP GET.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="f1fdc-135">**InternetSetOption**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="f1fdc-136">Establece una opción de Internet.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="f1fdc-137">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="f1fdc-138">Establece una función de devolución de llamada que recibe información de estado.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="f1fdc-139">Asigna una función de devolución de llamada al identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) designado y a todos los identificadores derivados de ella.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="f1fdc-140">**InternetUnlockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="f1fdc-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="f1fdc-141">Desbloquea un archivo que se ha bloqueado mediante la función [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="f1fdc-142">Leer archivos, buscar el siguiente archivo, manipular opciones y configurar operaciones asincrónicas es común a las funciones que admiten varios protocolos y tipos de identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="f1fdc-143">Leer archivos</span><span class="sxs-lookup"><span data-stu-id="f1fdc-143">Reading Files</span></span>

<span data-ttu-id="f1fdc-144">La función [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) se usa para descargar recursos de un [**identificador HINTERNET**](appendix-a-hinternet-handles.md) devuelto por la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="f1fdc-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) acepta una variable de puntero void que contiene la dirección de un búfer y un puntero a una variable que contiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="f1fdc-146">La función devuelve los datos en el búfer y la cantidad de datos descargados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="f1fdc-147">Las funciones WinINet proporcionan dos técnicas para descargar un recurso completo:</span><span class="sxs-lookup"><span data-stu-id="f1fdc-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="f1fdc-148">La función [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="f1fdc-149">Los valores devueltos de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="f1fdc-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) toma el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (después de llamar a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) en el identificador) y devuelve el número de bytes disponibles.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="f1fdc-151">La aplicación debe asignar un búfer igual al número de bytes disponibles, más 1 para el carácter **nulo** de terminación y usar ese búfer con [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="f1fdc-152">Este método no siempre funciona porque [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) comprueba el tamaño de archivo que aparece en el encabezado y no el archivo real.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="f1fdc-153">La información del archivo de encabezado podría estar obsoleta o falta el archivo de encabezado, ya que actualmente no es necesario en todos los estándares.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="f1fdc-154">En el ejemplo siguiente se lee el contenido del recurso al que tiene acceso el identificador hResource y se muestra en el cuadro de edición indicado por intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="f1fdc-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) devuelve cero bytes leídos y se completa correctamente cuando se han leído todos los datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="f1fdc-156">Esto permite que una aplicación use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) en un bucle para descargar los datos y salir cuando devuelva cero bytes leídos y se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="f1fdc-157">En el ejemplo siguiente se lee el recurso desde Internet y se muestra el recurso en el cuadro de edición indicado por intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="f1fdc-158">El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, fue devuelto por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (después de ser enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="f1fdc-159">Buscar el siguiente archivo</span><span class="sxs-lookup"><span data-stu-id="f1fdc-159">Finding the Next File</span></span>

<span data-ttu-id="f1fdc-160">La función [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) se usa para buscar el siguiente archivo en una búsqueda de archivos mediante los parámetros de búsqueda y el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="f1fdc-161">Para completar una búsqueda de archivos, siga llamando a [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) con el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) devuelto por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) hasta que se produzca un error en la función con el mensaje de error extendido [ \_ no hay \_ más \_ archivos](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="f1fdc-162">Para obtener la información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="f1fdc-163">En el ejemplo siguiente se muestra el contenido de un directorio FTP en el cuadro de lista indicado por lstDirectory.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="f1fdc-164">El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, es un identificador devuelto por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) después de establecer una sesión de FTP.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="f1fdc-165">Manipular opciones</span><span class="sxs-lookup"><span data-stu-id="f1fdc-165">Manipulating Options</span></span>

<span data-ttu-id="f1fdc-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) se usan para manipular las opciones de Wininet.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="f1fdc-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) acepta una variable que indica la opción que se va a establecer, un búfer para contener el valor de la opción y un puntero que contiene la dirección de la variable que contiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="f1fdc-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) acepta una variable que indica la opción de recuperación, un búfer para contener la configuración de opción y un puntero que contiene la dirección de la variable que contiene la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="f1fdc-169">Configurar operaciones asincrónicas</span><span class="sxs-lookup"><span data-stu-id="f1fdc-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="f1fdc-170">De forma predeterminada, las funciones WinINet funcionan sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="f1fdc-171">Una aplicación puede solicitar una operación asincrónica estableciendo la marca [ \_ \_ Async de marca de Internet](api-flags.md) en la llamada a la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="f1fdc-172">Todas las llamadas futuras realizadas en los identificadores derivados del identificador devuelto desde [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) se realizan de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="f1fdc-173">La lógica para la operación asincrónica frente a la sincrónica es permitir que una aplicación de un único subproceso Maximice su uso de la CPU sin tener que esperar a que se complete la e/s de red.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="f1fdc-174">Por lo tanto, dependiendo de la solicitud, la operación puede completarse de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="f1fdc-175">La aplicación debe comprobar el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-175">The application should check the return code.</span></span> <span data-ttu-id="f1fdc-176">Si una función devuelve **false** o **null**, y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ e/s \_ pendiente, la solicitud se ha realizado de forma asincrónica y se vuelve a llamar a la aplicación con la solicitud de estado de Internet \_ \_ \_ completa cuando se completa la función.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="f1fdc-177">Para comenzar la operación asincrónica, la aplicación debe establecer la [marca \_ \_ Async de marca de Internet](api-flags.md) en su llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="f1fdc-178">A continuación, la aplicación debe registrar una función de devolución de llamada válida mediante [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="f1fdc-179">Después de registrar una función de devolución de llamada para un identificador, todas las operaciones en ese identificador pueden generar indicaciones de estado, siempre que el valor de contexto que se proporcionó cuando se creó el identificador no sea cero.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="f1fdc-180">Proporcionar un valor de contexto cero obliga a que una operación se complete de forma sincrónica, aunque se especificó la [marca de Internet \_ \_ Async](api-flags.md) en [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="f1fdc-181">Las indicaciones de estado proporcionan a la aplicación comentarios sobre el progreso de las operaciones de red, como la resolución de un nombre de host, la conexión a un servidor y la recepción de datos.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="f1fdc-182">Se pueden realizar tres indicaciones de estado de uso especial para un identificador:</span><span class="sxs-lookup"><span data-stu-id="f1fdc-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="f1fdc-183">\_ \_ \_ El cierre del identificador de estado de Internet es la última indicación de estado que se realiza para un identificador.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="f1fdc-184">\_ \_ Identificador de estado \_ de Internet creado indica cuándo se crea inicialmente el identificador.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="f1fdc-185">La \_ solicitud de estado de Internet \_ \_ completa indica que se ha completado una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="f1fdc-186">La aplicación debe comprobar la estructura de [**\_ \_ resultados asincrónicos de Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) para determinar si la operación se realizó correctamente o no después de recibir una indicación de estado de Internet \_ \_ \_ rellenada.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="f1fdc-187">En el ejemplo siguiente se muestra un ejemplo de una función de devolución de llamada y una llamada a [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para registrar la función como la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="f1fdc-188">Cerrar los identificadores de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f1fdc-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="f1fdc-189">Todos los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) se pueden cerrar mediante la función [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="f1fdc-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="f1fdc-190">Las aplicaciones cliente deben cerrar todos los identificadores de **HINTERNET** derivados del identificador **HINTERNET** que están intentando cerrar antes de llamar a [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) en el identificador.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="f1fdc-191">En el ejemplo siguiente se muestra la jerarquía de identificadores.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="f1fdc-192">Bloquear y desbloquear recursos</span><span class="sxs-lookup"><span data-stu-id="f1fdc-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="f1fdc-193">La función [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permite a una aplicación asegurarse de que el recurso almacenado en caché asociado al identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que se ha pasado no desaparece de la caché.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="f1fdc-194">Si otra descarga intenta confirmar un recurso que tiene la misma dirección URL que el archivo bloqueado, la memoria caché evita la eliminación del archivo mediante una eliminación segura.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="f1fdc-195">Una vez que la aplicación llama a la función [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , se concede permiso a la memoria caché para eliminar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="f1fdc-196">Si se ha establecido la marca [Internet Flag not cache \_ \_ \_ \_ Write](api-flags.md) o [Internet \_ Flag not \_ \_ Cache](api-flags.md) , [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crea un archivo temporal con la extensión tmp, a menos que el identificador esté conectado a un recurso https.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="f1fdc-197">Si la función tiene acceso a un recurso https y a la marca de INTERNET no se ha \_ \_ \_ establecido ninguna escritura en caché \_ (o se ha establecido la marca de Internet como no \_ \_ \_ almacenada en caché), [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) produce un error.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="f1fdc-198">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="f1fdc-199">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="f1fdc-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f1fdc-200">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f1fdc-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
