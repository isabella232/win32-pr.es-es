---
description: Describe los archivos de entrada utilizados por WsdCodeGen y los archivos de salida generados por WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Acerca de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082444"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="e40ae-103">Acerca de WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="e40ae-103">About WsdCodeGen</span></span>

<span data-ttu-id="e40ae-104">WsdCodeGen usa un archivo de configuración XML para determinar la ubicación de los metadatos del servicio.</span><span class="sxs-lookup"><span data-stu-id="e40ae-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="e40ae-105">El archivo de configuración también se utiliza para definir los nombres de interfaz, los GUID de interfaz, los nombres de clase, los nombres de método y otros identificadores.</span><span class="sxs-lookup"><span data-stu-id="e40ae-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="e40ae-106">Para obtener más información sobre este archivo, vea [archivo de configuración WsdCodeGen](wsdcodegen-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="e40ae-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="e40ae-107">WsdCodeGen requiere dos tipos de archivos de entrada: un archivo de configuración XML y uno o más archivos de descripción de servicio (archivos WSDL o XSD).</span><span class="sxs-lookup"><span data-stu-id="e40ae-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="e40ae-108">WsdCodeGen procesa estos archivos de entrada y genera dos tipos de archivos de salida: archivos de interfaz y archivos de encabezado/origen.</span><span class="sxs-lookup"><span data-stu-id="e40ae-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="e40ae-109">Archivos de entrada</span><span class="sxs-lookup"><span data-stu-id="e40ae-109">Input Files</span></span>



| <span data-ttu-id="e40ae-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e40ae-110">Type</span></span>                      | <span data-ttu-id="e40ae-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e40ae-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e40ae-112">Archivo de configuración</span><span class="sxs-lookup"><span data-stu-id="e40ae-112">Configuration file</span></span>        | <span data-ttu-id="e40ae-113">Archivo XML que indica la ubicación de los metadatos del servicio y define los nombres de interfaz, los GUID de interfaz, los nombres de clase, los nombres de método y otros identificadores.</span><span class="sxs-lookup"><span data-stu-id="e40ae-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="e40ae-114">Archivos de descripción de servicio</span><span class="sxs-lookup"><span data-stu-id="e40ae-114">Service description files</span></span> | <span data-ttu-id="e40ae-115">Uno o más archivos WSDL o XSD que describen los servicios que se van a implementar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e40ae-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="e40ae-116">Archivos de resultados</span><span class="sxs-lookup"><span data-stu-id="e40ae-116">Output Files</span></span>



| <span data-ttu-id="e40ae-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="e40ae-117">Type</span></span>                        | <span data-ttu-id="e40ae-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e40ae-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e40ae-119">Archivos de interfaz</span><span class="sxs-lookup"><span data-stu-id="e40ae-119">Interface files</span></span>             | <span data-ttu-id="e40ae-120">Un archivo IDL (lenguaje de definición de interfaz) que se puede usar con el compilador MIDL para generar un archivo de encabezado de interfaz.</span><span class="sxs-lookup"><span data-stu-id="e40ae-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="e40ae-121">Los clientes WSDAPI y los servicios WSDAPI pueden utilizar este archivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="e40ae-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="e40ae-122">Archivos de encabezado y código fuente de C++</span><span class="sxs-lookup"><span data-stu-id="e40ae-122">C++ header and source files</span></span> | <span data-ttu-id="e40ae-123">Archivos de C++ que describen el contrato de mensaje, el espacio de nombres y la información de tipo.</span><span class="sxs-lookup"><span data-stu-id="e40ae-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="e40ae-124">Pueden contener código proxy o código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="e40ae-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="e40ae-125">El código proxy implementa la interfaz de un servicio y convierte las llamadas a métodos de servicio en operaciones de WSDAPI que realizan solicitudes de servicio.</span><span class="sxs-lookup"><span data-stu-id="e40ae-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="e40ae-126">El código auxiliar traduce las solicitudes del servicio WSDAPI en el código que llama a los métodos de servicio.</span><span class="sxs-lookup"><span data-stu-id="e40ae-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e40ae-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e40ae-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e40ae-128">Generador de código de servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="e40ae-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="e40ae-129">Usar WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="e40ae-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 



