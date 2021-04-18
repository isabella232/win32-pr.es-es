---
description: Obtiene una parte del cuerpo relacionada para la inserción en el flujo MHTML de salida.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'IItemPreviewerExt:: GetRelatedPart (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715017"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>IItemPreviewerExt:: GetRelatedPart (método)

Obtiene una parte del cuerpo relacionada para la inserción en el flujo MHTML de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwContext* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto para la operación. Invalide el valor predeterminado de **dwContext** para establecer el identificador de contexto en un valor de su elección.

</dd> <dt>

*pwszProp* \[ de\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero a la propiedad del contenido vinculado como una cadena Unicode.

</dd> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Valor entero largo sin signo que contiene el índice de base cero de la parte del cuerpo relacionada.

</dd> <dt>

*Pinfo* \[ out, retval\]
</dt> <dd>

Tipo: **[**LINKINFO**](-search-linkinfo.md) \** _

Recibe un puntero a la estructura [_ *LINKINFO* *](-search-linkinfo.md) en la que el método devuelve información sobre la transacción. *Pinfo* no debe ser un puntero **nulo** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




