---
description: Obtiene las interfaces de extensión que pueden ir con un controlador de dispositivo Windows Image Acquisition (WIA) 2.0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: Método IWiaItem2::GetExtension (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4c9738afe60d79b73149c9dd7dda8c3bbd1017c3b41d023b47160b624bcd7c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450424"
---
# <a name="iwiaitem2getextension-method"></a>IWiaItem2::GetExtension (método)

Obtiene las interfaces de extensión que pueden ir con un controlador de dispositivo Windows Image Acquisition (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la extensión a la que la aplicación que realiza la llamada requiere un puntero.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

Extensión de filtro de segmentación. Este es actualmente el único valor válido para este parámetro.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ En\]
</dt> <dd>

Tipo: **REFIID**

Especifica el identificador de la interfaz de extensión.

</dd> <dt>

*ppOut* \[ out\]
</dt> <dd>

Tipo: **\* \* VOID**

Recibe la dirección de un puntero a la interfaz de extensión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Una aplicación invoca este método para crear un objeto de extensión que implementa una de las interfaces de extensión del controlador WIA 2.0. **IWiaItem2::GetExtension** almacena la dirección de la interfaz de extensión del objeto de extensión en el *parámetro riidExtensionInterface.* A continuación, la aplicación usa el puntero de interfaz para llamar a sus métodos.

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *riidExtensionInterface.*

## <a name="examples"></a>Ejemplos

CreateSegmentationFilter crea una instancia del filtro de segmentación del controlador ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) llamando a **IWiaItem2::GetExtension** en la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) pasada.


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
