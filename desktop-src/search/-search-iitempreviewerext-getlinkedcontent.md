---
description: Permite la extensión a contenido enriquecido para una propiedad.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: IItemPreviewerExt::GetLinkedContent (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9b99d46d33ba66a9669d47021661b0a359fb2ca98d418735238e2baf3dc9e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094926"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>IItemPreviewerExt::GetLinkedContent (método)

Permite la extensión a contenido enriquecido para una propiedad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwContext* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto de la operación. Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.

</dd> <dt>

*pwszProp* \[ En\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero a la propiedad del contenido vinculado como una cadena Unicode.

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

La [**interfaz IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y Windows Server 2003, y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las SIGUIENTES API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




