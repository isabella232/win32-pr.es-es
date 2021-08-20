---
description: Obtiene una parte del cuerpo relacionada para insertarla en la secuencia MHTML de salida.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: IItemPreviewerExt::GetRelatedPart (método)
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
ms.openlocfilehash: 9abc4415eef014697376c9df4b89af47037a99df5c9ab5a3c74a3d7825b344c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863978"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>IItemPreviewerExt::GetRelatedPart (método)

Obtiene una parte del cuerpo relacionada para insertarla en la secuencia MHTML de salida.

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

*dwContext* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto de la operación. Invalide el valor predeterminado de **dwContext** para establecer el identificador de contexto en el valor que elija.

</dd> <dt>

*pwszProp* \[ En\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero a la propiedad del contenido vinculado como una cadena Unicode.

</dd> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Valor entero largo sin signo que contiene el índice de base cero de la parte del cuerpo relacionada.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LINKINFO**](-search-linkinfo.md)\***

Recibe un puntero a la [**estructura LINKINFO**](-search-linkinfo.md) en la que el método devuelve información sobre la transacción. *pInfo* no debe ser un **puntero NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**interfaz IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




