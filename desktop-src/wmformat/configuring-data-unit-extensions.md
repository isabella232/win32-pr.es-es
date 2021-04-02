---
title: Configuración de extensiones de unidades de datos
description: Configuración de extensiones de unidades de datos
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- flujos, configurar extensiones de unidad de datos
- secuencias, extensiones de unidad de datos
- extensiones de unidad de datos, configurar
- perfiles, extensiones de unidad de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789183"
---
# <a name="configuring-data-unit-extensions"></a><span data-ttu-id="84923-107">Configuración de extensiones de unidades de datos</span><span class="sxs-lookup"><span data-stu-id="84923-107">Configuring Data Unit Extensions</span></span>

<span data-ttu-id="84923-108">Los ejemplos escritos en archivos ASF pueden contener información adicional aparte de los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="84923-108">Samples written to ASF files can contain additional information apart from the media samples themselves.</span></span> <span data-ttu-id="84923-109">Esta información se incluye con las extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="84923-109">This information is included using data unit extensions.</span></span> <span data-ttu-id="84923-110">Para obtener más información acerca de las extensiones de unidad de datos, consulte [extensiones de unidad de datos](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="84923-110">For more information about data unit extensions, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="84923-111">Para usar las extensiones de unidad de datos, debe configurar la secuencia en el perfil para que las acepte.</span><span class="sxs-lookup"><span data-stu-id="84923-111">To use data unit extensions, you must configure the stream in the profile to accept them.</span></span> <span data-ttu-id="84923-112">Para configurar una extensión de unidad de datos para una secuencia, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="84923-112">To configure a data unit extension for a stream, perform the following steps.</span></span>

1.  <span data-ttu-id="84923-113">Obtenga un puntero a la interfaz [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) llamando al método **QueryInterface** de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="84923-113">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface by calling the **QueryInterface** method of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span>
2.  <span data-ttu-id="84923-114">Llame a [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para registrar un tipo de extensión de unidad de datos para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="84923-114">Call [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) to register a type of data unit extension for the stream.</span></span>

<span data-ttu-id="84923-115">Puede examinar todos los tipos de extensión de unidad de datos registrados actualmente para una secuencia llamando a [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) para recuperar el número de tipos de extensión de unidad de datos registrados.</span><span class="sxs-lookup"><span data-stu-id="84923-115">You can examine all of the data unit extension types currently registered for a stream by calling [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) to retrieve the number of registered data unit extension types.</span></span> <span data-ttu-id="84923-116">A continuación, puede recorrer todos los tipos mediante llamadas a [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) para cada uno.</span><span class="sxs-lookup"><span data-stu-id="84923-116">Then you can loop through all of the types using calls to [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) for each.</span></span>

<span data-ttu-id="84923-117">A las extensiones de unidad de datos se les asigna un tamaño cuando se configuran para un flujo.</span><span class="sxs-lookup"><span data-stu-id="84923-117">Data unit extensions are assigned a size when configured for a stream.</span></span> <span data-ttu-id="84923-118">Muchos sistemas de extensión de unidad de datos usan datos que tienen un tamaño constante (normalmente una estructura).</span><span class="sxs-lookup"><span data-stu-id="84923-118">Many data unit extension systems use data that is a constant size (usually a structure).</span></span> <span data-ttu-id="84923-119">Sin embargo, también puede configurar las extensiones de unidad de datos para que tengan un tamaño variable al establecer el tamaño en 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="84923-119">However, you can also configure your data unit extensions to be of variable size by setting the size to 0xFFFF.</span></span> <span data-ttu-id="84923-120">Cada extensión de unidad de datos asignada en el momento de la codificación puede tener cualquier tamaño entre 1 byte y 65534 bytes.</span><span class="sxs-lookup"><span data-stu-id="84923-120">Each data unit extension assigned at encoding time can then be of any size between 1 byte and 65534 bytes.</span></span> <span data-ttu-id="84923-121">Las extensiones de unidad de datos de tamaño variable también se denominan extensiones de unidad de datos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="84923-121">Variably sized data unit extensions are also called dynamic data unit extensions.</span></span>

<span data-ttu-id="84923-122">La ventaja de usar las extensiones de unidad de datos dinámicas es que puede adjuntar datos de extensión según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="84923-122">The advantage of using dynamic data unit extensions is that you can attach extension data as needed.</span></span> <span data-ttu-id="84923-123">Si define una extensión de unidad de datos con un tamaño establecido, cada muestra de la secuencia debe contener datos de extensión de ese tamaño, aunque no tenga datos para algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="84923-123">If you define a data unit extension with a set size, every sample for the stream must contain extension data of that size, even if you have no data for some samples.</span></span> <span data-ttu-id="84923-124">Con las extensiones de unidad de datos dinámicos, puede omitir las extensiones de unidad de datos de algunos ejemplos, lo que ahorra espacio y reduce los requisitos de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="84923-124">With dynamic data unit extensions, you can omit data unit extensions from some samples, which saves space and reduces bandwidth requirements.</span></span> <span data-ttu-id="84923-125">Sin embargo, si las extensiones de unidad de datos son de tamaño variable, el objeto de lectura no puede comprobar los datos de la extensión recibida con respecto a un tamaño estático.</span><span class="sxs-lookup"><span data-stu-id="84923-125">However, if data unit extensions are of variable size, the reading object cannot verify the received extension data against a static size.</span></span> <span data-ttu-id="84923-126">Debe comprobar que los datos de la extensión que recibe son válidos, y no la distorsión malintencionada del flujo de bits.</span><span class="sxs-lookup"><span data-stu-id="84923-126">You must verify that the extension data that you receive is valid, and not malicious distortion of the bit stream.</span></span>

<span data-ttu-id="84923-127">Las extensiones de unidad de datos individuales deben establecerse en ejemplos mediante el método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="84923-127">Individual data unit extensions must be set on samples by using the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="84923-128">Para obtener más información, consulte [configuración de las extensiones de unidad de datos](setting-data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="84923-128">For more information, see [Setting Data Unit Extensions](setting-data-unit-extensions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84923-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84923-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84923-130">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="84923-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




