---
description: Obtiene la información necesaria para leer o guardar las propiedades en el contenedor de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'IItemPropertyBag:: GetPropertyInfo (método)'
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
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714997"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>IItemPropertyBag:: GetPropertyInfo (método)

Obtiene la información necesaria para leer o guardar las propiedades en el contenedor de propiedades. La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

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

*iProperty* \[ de\]
</dt> <dd>

Índice de base cero de la primera propiedad para la que se solicita información.

</dd> <dt>

*cProperties* \[ de\]
</dt> <dd>

Número de propiedades para las que se va a obtener información. Este argumento especifica el número de elementos de matriz en *pPropBag*.

</dd> <dt>

*pPropBag* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de estructuras [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que recibe la información de las propiedades.

</dd> <dt>

*pcProperties* \[ enuncia\]
</dt> <dd>

Recibe un puntero a una variable **ULong** que recibe el número de propiedades para las que se recuperó la información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPropertyBag**](iitempropertybag.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) y [**ISearchItem**](-search-isearchitem.md) , las estructuras [**LINKINFO**](-search-linkinfo.md) y [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) y la enumeración [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




