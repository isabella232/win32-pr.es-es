---
description: Hace que una o varias propiedades se lean desde el bolsa de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: IItemPropertyBag::Read (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c04cf34720871b1254f16822a090f48f8d68aaeb82398744d5139486fb6dd2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226610"
---
# <a name="iitempropertybagread-method"></a>IItemPropertyBag::Read (método)

Hace que una o varias propiedades se lean desde el bolsa de propiedades. La [**interfaz IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP Windows Server 2003 y ya no se debe usar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cProperties* \[ En\]
</dt> <dd>

Número de propiedades que se leerán. Este argumento especifica el número de elementos de las matrices en *pPropBag,* *pvarValue* y *phrError*.

</dd> <dt>

*pPropBag* \[ En\]
</dt> <dd>

Puntero a una matriz de [**estructuras ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica las propiedades que se solicitan.

</dd> <dt>

*pvarValue* \[ out\]
</dt> <dd>

Recibe un puntero que devuelve una matriz de **estructuras VARIANT** que recibe los valores de propiedad.

</dd> <dt>

*phrError* \[ out\]
</dt> <dd>

Puntero a una matriz de **valores HRESULT** que recibe el resultado de cada propiedad leída. Debe haber al menos *elementos cProperties* en esta matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**interfaz IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulta también

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




