---
description: 'Comprueba si una extensión especificada está disponible en el equipo y puede ser utilizada por el método IWiaItem2:: GetExtension.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2:: CheckExtension (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715343"
---
# <a name="iwiaitem2checkextension-method"></a>IWiaItem2:: CheckExtension (método)

Comprueba si una extensión especificada está disponible en el equipo y puede ser utilizada por el método [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
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

Especifica el nombre de la extensión.

</dd> <dt>

*riidExtensionInterface* \[ de\]
</dt> <dd>

Tipo: **REFIID**

Actualmente no se usa.

</dd> <dt>

*pbExtensionExists* \[ enuncia\]
</dt> <dd>

Tipo: **bool \** _

Recibe un puntero a un _ * BOOL * *.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**ES**


</dt> <dd>

La extensión especificada no está disponible.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**REALES**


</dt> <dd>

La extensión especificada está disponible.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Con este método, las aplicaciones pueden comprobar si una extensión está disponible antes de llamar al método [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) . Además, la aplicación puede comprobar qué extensiones están disponibles sin crear conjuntamente cada una de ellas y, a continuación, decidir cuál usar.

## <a name="examples"></a>Ejemplos

CheckImgFilter comprueba si el controlador tiene un filtro de procesamiento de imágenes. Antes de llamar al componente de vista previa, una aplicación debe asegurarse de que el controlador tiene un filtro de procesamiento de imágenes.


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
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



 

 




