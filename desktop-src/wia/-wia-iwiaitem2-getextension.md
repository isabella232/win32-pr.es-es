---
description: Obtiene las interfaces de extensión que pueden presentarse con un controlador de dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2:: GetExtension (método) (WIA. h)'
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
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082149"
---
# <a name="iwiaitem2getextension-method"></a>IWiaItem2:: GetExtension (método)

Obtiene las interfaces de extensión que pueden presentarse con un controlador de dispositivo de adquisición de imágenes de Windows (WIA) 2,0.

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

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la extensión a la que la aplicación que realiza la llamada requiere un puntero.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

La extensión del filtro de segmentación. Este es actualmente el único valor válido para este parámetro.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ de\]
</dt> <dd>

Tipo: **REFIID**

Especifica el identificador de la interfaz de extensión.

</dd> <dt>

*ppOut* \[ enuncia\]
</dt> <dd>

Tipo: **void \* \***

Recibe la dirección de un puntero a la interfaz de extensión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Una aplicación invoca este método para crear un objeto de extensión que implementa una de las interfaces de extensión de controlador de WIA 2,0. **IWiaItem2:: getExtension** almacena la dirección de la interfaz de extensión del objeto de extensión en el parámetro *riidExtensionInterface* . A continuación, la aplicación usa el puntero de interfaz para llamar a sus métodos.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *riidExtensionInterface* .

## <a name="examples"></a>Ejemplos

CreateSegmentationFilter crea una instancia del filtro de segmentación del controlador ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) llamando a **IWiaItem2:: getExtension** en la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) pasada.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
