---
description: Cuando el codificador de Windows Media Audio enumera los tipos de salida, identifica cada tipo enumerado como estándar, profesional o sin pérdida.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configuración de la codificación de audio estándar, profesional o sin pérdida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808150"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="c7a9b-103">Configuración de la codificación de audio estándar, profesional o sin pérdida</span><span class="sxs-lookup"><span data-stu-id="c7a9b-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="c7a9b-104">Cuando el codificador de Windows Media Audio enumera los tipos de salida, identifica cada tipo enumerado como estándar, profesional o sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="c7a9b-105">Puede determinar si un tipo de salida es Standard, Professional o Lossless realizando los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="c7a9b-106">Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener una interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que represente el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="c7a9b-107">Llame a [**IMFMediaType:: GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) para obtener una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contenga información sobre el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="c7a9b-108">El miembro **pbFormat** de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) apunta a una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que contiene información adicional sobre el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="c7a9b-109">Inspeccione el miembro **wFormatTag** de la estructura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="c7a9b-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="c7a9b-110">Un valor de 0x161 indica Standard, un valor de 0x162 indica Professional y un valor de 0x163 indica Lossless.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="c7a9b-111">Si establece propiedades en el codificador Windows Media Audio antes de enumerar los tipos de salida, puede limitar el número de tipos de salida que se enumeran.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="c7a9b-112">Por ejemplo, si establece las propiedades de VBR adecuadamente, puede limitar los tipos de salida enumerados a los que se encuentran en la categoría sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="c7a9b-113">Codificación de audio estándar</span><span class="sxs-lookup"><span data-stu-id="c7a9b-113">Standard Audio Encoding</span></span>

<span data-ttu-id="c7a9b-114">Puede usar los pasos siguientes para configurar la codificación de audio estándar.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="c7a9b-115">Establezca las propiedades de su elección en el codificador.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="c7a9b-116">Enumera los posibles tipos de salida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="c7a9b-117">Inspeccione los tipos enumerados y elija uno que tenga una etiqueta de formato de audio de 0x161.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="c7a9b-118">Establezca el tipo de salida en el tipo elegido llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c7a9b-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="c7a9b-119">Codificación de audio profesional</span><span class="sxs-lookup"><span data-stu-id="c7a9b-119">Professional Audio Encoding</span></span>

<span data-ttu-id="c7a9b-120">Puede usar los pasos siguientes para configurar la codificación de audio profesional.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="c7a9b-121">Establezca las propiedades de su elección en el codificador.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="c7a9b-122">Enumera los posibles tipos de salida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="c7a9b-123">Inspeccione los tipos enumerados y elija uno que tenga una etiqueta de formato de audio de 0x162.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="c7a9b-124">Establezca el tipo de salida en el tipo elegido llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c7a9b-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="c7a9b-125">Codificación de audio sin pérdida</span><span class="sxs-lookup"><span data-stu-id="c7a9b-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="c7a9b-126">Puede usar los pasos siguientes para configurar la codificación de audio sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="c7a9b-127">Establezca la propiedad [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="c7a9b-128">Establezca la propiedad [**MFPKEY de \_ restricción \_ enumerada \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="c7a9b-129">Establezca la [**propiedad \_ \_ VBRQUALITY deseada de MFPKEY**](mfpkey-desired-vbrqualityproperty.md) en 100.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="c7a9b-130">Enumerar los tipos de salida.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="c7a9b-131">Establezca el tipo de salida en uno de los tipos enumerados en el paso 4 llamando a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c7a9b-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="c7a9b-132">En el código siguiente se enumeran todos los tipos de salida sin pérdida para el codificador Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="c7a9b-133">El código imprime el valor de la etiqueta de formato de audio para cada tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="c7a9b-134">Dado que todos los tipos enumerados son sin pérdida, todas esas etiquetas de formato tienen un valor de 0x163.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="c7a9b-135">Supongamos que pIMT es un puntero a una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un objeto de codificador Windows Media Audio y que pStore es un puntero a una interfaz **IPropertyStore** en el mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="c7a9b-136">Supongamos también que HR es una variable de tipo **HRESULT** que se declaró anteriormente en el código.</span><span class="sxs-lookup"><span data-stu-id="c7a9b-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a><span data-ttu-id="c7a9b-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7a9b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a9b-138">Configuración de la codificación de audio</span><span class="sxs-lookup"><span data-stu-id="c7a9b-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
