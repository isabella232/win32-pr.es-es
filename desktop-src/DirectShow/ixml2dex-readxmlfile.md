---
description: El método ReadXMLFile carga un archivo de proyecto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex:: ReadXMLFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690916"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="ca8ed-103">IXml2Dex:: ReadXMLFile (método)</span><span class="sxs-lookup"><span data-stu-id="ca8ed-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="ca8ed-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-104">\[Deprecated.</span></span> <span data-ttu-id="ca8ed-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ca8ed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ca8ed-106">El `ReadXMLFile` método carga un archivo de proyecto XML.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="ca8ed-107">Este método crea instancias de todos los objetos expresados en el archivo XML y los inserta en la escala de tiempo, así como la aplicación de los atributos proporcionados para la escala de tiempo, como la velocidad de fotogramas o el efecto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca8ed-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="ca8ed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca8ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca8ed-110">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="ca8ed-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="ca8ed-111">Puntero a la interfaz **IUnknown** de un objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="ca8ed-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="ca8ed-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="ca8ed-113">Cadena que especifica el nombre del archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca8ed-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca8ed-114">Return value</span></span>

<span data-ttu-id="ca8ed-115">Devuelve un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-115">Returns an HRESULT value.</span></span> <span data-ttu-id="ca8ed-116">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-116">Possible values include the following.</span></span>



| <span data-ttu-id="ca8ed-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ca8ed-117">Return code</span></span>                                                                                                  | <span data-ttu-id="ca8ed-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca8ed-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="ca8ed-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ca8ed-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="ca8ed-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="ca8ed-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="ca8ed-121"><dt>**\_formato de \_ archivo no válido de VFW E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca8ed-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="ca8ed-122">Formato de archivo no válido</span><span class="sxs-lookup"><span data-stu-id="ca8ed-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca8ed-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca8ed-123">Remarks</span></span>

<span data-ttu-id="ca8ed-124">Este método no borra los objetos existentes de la escala de tiempo antes de insertar los nuevos objetos definidos en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="ca8ed-125">Si necesita actualizar una escala de tiempo existente, llame a [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="ca8ed-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ca8ed-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ca8ed-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ca8ed-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ca8ed-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca8ed-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca8ed-129">Requirements</span></span>



| <span data-ttu-id="ca8ed-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca8ed-130">Requirement</span></span> | <span data-ttu-id="ca8ed-131">Value</span><span class="sxs-lookup"><span data-stu-id="ca8ed-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8ed-132">Versión</span><span class="sxs-lookup"><span data-stu-id="ca8ed-132">Version</span></span><br/> | <span data-ttu-id="ca8ed-133">Internet Explorer 4,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ca8ed-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="ca8ed-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca8ed-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ca8ed-135"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca8ed-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ca8ed-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca8ed-136">Library</span></span><br/> | <dl> <span data-ttu-id="ca8ed-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca8ed-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca8ed-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca8ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca8ed-139">**Interfaz IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="ca8ed-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="ca8ed-140">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="ca8ed-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




