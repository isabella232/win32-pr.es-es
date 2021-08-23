---
description: Comprueba si una extensión especificada está disponible en la máquina y la puede usar el método IWiaItem2::GetExtension.
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: Método IWiaItem2::CheckExtension (Wia.h)
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
ms.openlocfilehash: 50240fbf10155fae555c6cd2e30bf8c86c571b8d52b86e02eab9f5bb11ac17ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965584"
---
# <a name="iwiaitem2checkextension-method"></a>IWiaItem2::CheckExtension (método)

Comprueba si una extensión especificada está disponible en la máquina y la puede usar el [**método IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md)

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la extensión.

</dd> <dt>

*riidExtensionInterface* \[ En\]
</dt> <dd>

Tipo: **REFIID**

Actualmente no se usa.

</dd> <dt>

*pbExtensionExists* \[ out\]
</dt> <dd>

Tipo: **BOOL \***

Recibe un puntero a **un objeto BOOL.**

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**Falso**


</dt> <dd>

La extensión especificada no está disponible.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdad**


</dt> <dd>

La extensión especificada está disponible.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Con este método, las aplicaciones pueden comprobar si una extensión está disponible antes de llamar al [**método IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md) Además, la aplicación puede comprobar qué extensiones están disponibles sin crear de forma coofiera cada una de ellas y, a continuación, decidir cuál usar.

## <a name="examples"></a>Ejemplos

CheckImgFilter comprueba si el controlador tiene un filtro de procesamiento de imágenes. Antes de llamar al componente de versión preliminar, una aplicación debe asegurarse de que el controlador tiene un filtro de procesamiento de imágenes.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




