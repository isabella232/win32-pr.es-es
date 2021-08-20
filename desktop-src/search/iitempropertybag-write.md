---
description: Hace que una o varias propiedades se guarden en el bolsa de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: IItemPropertyBag::Write (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: e8860653244cef53739c7d104405a176c1ec63d2de1d3434b1d25e3206c431aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863114"
---
# <a name="iitempropertybagwrite-method"></a>IItemPropertyBag::Write (Método)

Hace que una o varias propiedades se guarden en el bolsa de propiedades. La [**interfaz IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y Windows Server 2003, y ya no se debe usar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cProperties* \[ En\]
</dt> <dd>

Número de propiedades que se guardarán. Este argumento especifica el número de elementos de las matrices en *pPropBag* y *pvarValue.*

</dd> <dt>

*pPropBag* \[ En\]
</dt> <dd>

Puntero a una matriz de [**estructuras ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica las propiedades que se guardarán.

</dd> <dt>

*pvarValue* \[ En\]
</dt> <dd>

Puntero a **un variant cuyo** tipo depende del tipo de datos de la información de propiedad que contiene.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**interfaz IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y Windows Server 2003, y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




