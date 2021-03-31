---
description: Los registros de WSDAPI contienen información de depuración que se puede usar para encontrar la causa principal de los errores de aplicación de WSDAPI.
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: Habilitar el seguimiento de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951f8ddfee6043cc662a456c70960e78ed1a3625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082442"
---
# <a name="enabling-wsdapi-tracing"></a><span data-ttu-id="de9e3-103">Habilitar el seguimiento de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="de9e3-103">Enabling WSDAPI Tracing</span></span>

<span data-ttu-id="de9e3-104">Los registros de WSDAPI contienen información de depuración que se puede usar para encontrar la causa principal de los errores de aplicación de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="de9e3-104">WSDAPI logs contain debugging information that can be used to find the root cause of WSDAPI application failures.</span></span> <span data-ttu-id="de9e3-105">Cuando el seguimiento está habilitado, la información de registro se almacena en un archivo. ETL en una ubicación especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="de9e3-105">When tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="de9e3-106">Este archivo. ETL se puede enviar al soporte técnico de Microsoft para desarrolladores para el análisis de la causa principal.</span><span class="sxs-lookup"><span data-stu-id="de9e3-106">This .etl file can be sent to Microsoft developer support for root cause analysis.</span></span> <span data-ttu-id="de9e3-107">Para obtener información sobre cómo ponerse en contacto con el soporte técnico, vaya a [https://support.microsoft.com](https://support.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="de9e3-107">For information about contacting support, go to [https://support.microsoft.com](https://support.microsoft.com).</span></span>

<span data-ttu-id="de9e3-108">Este procedimiento debe realizarse dos veces: una vez en el cliente y otra en el host.</span><span class="sxs-lookup"><span data-stu-id="de9e3-108">This procedure must be done twice: once on the client, and once on the host.</span></span>

<span data-ttu-id="de9e3-109">**Para habilitar el seguimiento de WSDAPI**</span><span class="sxs-lookup"><span data-stu-id="de9e3-109">**To enable WSDAPI tracing**</span></span>

1.  <span data-ttu-id="de9e3-110">Con el Bloc de notas u otro editor de texto, cree un archivo de texto con el siguiente texto:</span><span class="sxs-lookup"><span data-stu-id="de9e3-110">Using Notepad or another text editor, create a text file with the following text:</span></span>

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  <span data-ttu-id="de9e3-111">Guarde el archivo de texto como `C:\temp\traceguids.txt` y, a continuación, cierre el archivo.</span><span class="sxs-lookup"><span data-stu-id="de9e3-111">Save the text file as `C:\temp\traceguids.txt` and then close the file.</span></span>
3.  <span data-ttu-id="de9e3-112">Abra una ventana del símbolo del sistema con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="de9e3-112">Open an elevated command prompt window.</span></span>
4.  <span data-ttu-id="de9e3-113">Ejecute el siguiente comando: **logman.exe Create Trace wsdlog-o c: \\ temp \\ WSD**</span><span class="sxs-lookup"><span data-stu-id="de9e3-113">Run the following command: **logman.exe create trace wsdlog -o c:\\temp\\wsd**</span></span>
5.  <span data-ttu-id="de9e3-114">Ejecute el siguiente comando: **logman.exe Update wsdlog-PF c: \\ temp \\traceguids.txt**</span><span class="sxs-lookup"><span data-stu-id="de9e3-114">Run the following command: **logman.exe update wsdlog -pf c:\\temp\\traceguids.txt**</span></span>
6.  <span data-ttu-id="de9e3-115">Ejecute el siguiente comando: **logman.exe Start wsdlog**</span><span class="sxs-lookup"><span data-stu-id="de9e3-115">Run the following command: **logman.exe start wsdlog**</span></span>
7.  <span data-ttu-id="de9e3-116">Reproduzca el error iniciando el host y el cliente, o presionando F5 en el explorador de red.</span><span class="sxs-lookup"><span data-stu-id="de9e3-116">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>

<span data-ttu-id="de9e3-117">**Para deshabilitar el seguimiento de WSDAPI**</span><span class="sxs-lookup"><span data-stu-id="de9e3-117">**To disable WSDAPI tracing**</span></span>

1.  <span data-ttu-id="de9e3-118">Abra una ventana del símbolo del sistema con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="de9e3-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="de9e3-119">Ejecute el siguiente comando: **logman.exe STOP wsdlog**</span><span class="sxs-lookup"><span data-stu-id="de9e3-119">Run the following command: **logman.exe stop wsdlog**</span></span>

<span data-ttu-id="de9e3-120">Una vez capturado el error de aplicación, los \* archivos. ETL se pueden enviar al soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="de9e3-120">Once the application failure has been captured, the \*.etl files can be sent to Microsoft support.</span></span> <span data-ttu-id="de9e3-121">Estos archivos se encuentran en `C:\temp\wsd_*.etl` .</span><span class="sxs-lookup"><span data-stu-id="de9e3-121">These files are located in `C:\temp\wsd_*.etl`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de9e3-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de9e3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de9e3-123">Procedimientos de diagnóstico de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="de9e3-123">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="de9e3-124">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="de9e3-124">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



