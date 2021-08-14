---
description: Obtiene la información necesaria para leer o guardar las propiedades en el bolsa de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: IItemPropertyBag::GetPropertyInfo (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7a69ceff2236a101f18ee06b4a87dd60e35ca69e73fdeb085232f102f8450d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863094"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>IItemPropertyBag::GetPropertyInfo (método)

Obtiene la información necesaria para leer o guardar las propiedades en el bolsa de propiedades. La [**interfaz IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iProperty* \[ En\]
</dt> <dd>

Índice de base cero de la primera propiedad para la que se solicita información.

</dd> <dt>

*cProperties* \[ En\]
</dt> <dd>

Número de propiedades para las que se obtiene información. Este argumento especifica el número de elementos de matriz en *pPropBag.*

</dd> <dt>

*pPropBag* \[ out\]
</dt> <dd>

Puntero a una matriz de [**estructuras ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que recibe la información de las propiedades.

</dd> <dt>

*pcProperties* \[ out\]
</dt> <dd>

Recibe un puntero a una variable **ULONG** que recibe el número de propiedades para las que se recuperó la información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**interfaz IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




