---
description: Describe cómo usar la herramienta de búsqueda de errores de Microsoft para buscar explicaciones de texto de códigos de error hexadecimales en Windows.
title: Herramienta de búsqueda de errores de Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720278"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="f5f53-103">Herramienta de búsqueda de errores de Microsoft</span><span class="sxs-lookup"><span data-stu-id="f5f53-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="f5f53-104">La herramienta de búsqueda de errores de Microsoft muestra el texto del mensaje que está asociado a un código de estado hexadecimal (u otro código).</span><span class="sxs-lookup"><span data-stu-id="f5f53-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="f5f53-105">Este texto se define en varios archivos de encabezado de código fuente de Microsoft, como Winerror. h, setupapi. h, etc.</span><span class="sxs-lookup"><span data-stu-id="f5f53-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="f5f53-106">La herramienta está firmada digitalmente por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5f53-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="f5f53-107">A continuación se encuentra la información de SHA256 para la descarga de archivos:</span><span class="sxs-lookup"><span data-stu-id="f5f53-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="f5f53-108">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="f5f53-108">Algorithm</span></span> |<span data-ttu-id="f5f53-109">Hash</span><span class="sxs-lookup"><span data-stu-id="f5f53-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="f5f53-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="f5f53-110">SHA256</span></span> |<span data-ttu-id="f5f53-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span><span class="sxs-lookup"><span data-stu-id="f5f53-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="f5f53-112">Los entornos empresariales pueden restringir qué archivos pueden ejecutarse y desde dónde.</span><span class="sxs-lookup"><span data-stu-id="f5f53-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="f5f53-113">Antes de descargar y ejecutar esta herramienta, compruebe los detalles siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5f53-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="f5f53-114">¿Tiene que tener permiso o una excepción de seguridad para descargar o ejecutar la herramienta?</span><span class="sxs-lookup"><span data-stu-id="f5f53-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="f5f53-115">¿Puede almacenar y ejecutar esta herramienta en el equipo (por ejemplo, en la carpeta documentos)?</span><span class="sxs-lookup"><span data-stu-id="f5f53-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="f5f53-116">¿O tiene que almacenar y ejecutar la herramienta en un equipo especializado, como un servidor de archivos central?</span><span class="sxs-lookup"><span data-stu-id="f5f53-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="f5f53-117">Uso</span><span class="sxs-lookup"><span data-stu-id="f5f53-117">Usage</span></span>

1. <span data-ttu-id="f5f53-118">Descargue la herramienta seleccionando [este vínculo](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span><span class="sxs-lookup"><span data-stu-id="f5f53-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="f5f53-119">Si no especificó una ubicación en el paso 1, vaya a la carpeta de descarga y copie o mueva el archivo descargado (Err_6.4.5.exe) a la carpeta en la que se almacenará la herramienta.</span><span class="sxs-lookup"><span data-stu-id="f5f53-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="f5f53-120">No es necesario expandir ni instalar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f5f53-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="f5f53-121">Si copia o mueve el archivo a una carpeta que aparece en la variable de entorno **path** de su sistema operativo, funcionará en cualquier símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5f53-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="f5f53-122">Abra una ventana de símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5f53-122">Open a Command Prompt window.</span></span> <span data-ttu-id="f5f53-123">Si es necesario, cambie el directorio a la ubicación de la herramienta de búsqueda de errores.</span><span class="sxs-lookup"><span data-stu-id="f5f53-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="f5f53-124">Ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="f5f53-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="f5f53-125">En este comando, \<*error code*> representa el código hexadecimal que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="f5f53-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="f5f53-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5f53-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="f5f53-127">Más información</span><span class="sxs-lookup"><span data-stu-id="f5f53-127">More information</span></span>

<span data-ttu-id="f5f53-128">Tenga en cuenta que se trata de una herramienta "momento dado".</span><span class="sxs-lookup"><span data-stu-id="f5f53-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="f5f53-129">La herramienta de búsqueda de errores de Microsoft descodifica la mayoría de los códigos de error de Microsoft a partir de la fecha en la que se compiló la herramienta.</span><span class="sxs-lookup"><span data-stu-id="f5f53-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="f5f53-130">A medida que nuevas versiones de Windows agregan nuevos eventos y códigos de error, es posible que tenga que descargar una nueva versión de la herramienta de búsqueda de errores.</span><span class="sxs-lookup"><span data-stu-id="f5f53-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="f5f53-131">Consulte el centro de descarga de Microsoft para obtener una nueva versión o vea los [códigos de error](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f5f53-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
