---
description: Hace que una o más propiedades se lean del contenedor de propiedades. La interfaz IItemPropertyBag solo se admite en Windows XP y Windows Server 2003, y ya no debe usarse.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'IItemPropertyBag:: Read (método)'
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
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360187"
---
# <a name="iitempropertybagread-method"></a>IItemPropertyBag:: Read (método)

Hace que una o más propiedades se lean del contenedor de propiedades. La interfaz [**IItemPropertyBag**](iitempropertybag.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

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

*cProperties* \[ de\]
</dt> <dd>

Número de propiedades que se van a leer. Este argumento especifica el número de elementos de las matrices en *pPropBag*, *pvarValue* y *phrError*.

</dd> <dt>

*pPropBag* \[ de\]
</dt> <dd>

Puntero a una matriz de estructuras [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica las propiedades que se solicitan.

</dd> <dt>

*pvarValue* \[ enuncia\]
</dt> <dd>

Recibe un puntero que devuelve una matriz de estructuras **variantes** que recibe los valores de propiedad.

</dd> <dt>

*phrError* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de valores **HRESULT** que recibe el resultado de cada lectura de propiedad. Debe haber al menos *cProperties* elementos en esta matriz.

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

 

 




