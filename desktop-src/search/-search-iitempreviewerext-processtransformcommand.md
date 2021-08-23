---
description: Permite el procesamiento de un comando de transformación encontrado en una plantilla de vista previa.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt::P rocessTransformCommand (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: f93d4be0bf9491c4fd2f6074c00692d6f634704ec820a34baeb4f1d52343c36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969784"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt::P rocessTransformCommand (método)

Permite el procesamiento de un comando de transformación encontrado en una plantilla de vista previa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwContext* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto de la operación. Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.

</dd> <dt>

*pwszName* \[ En\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero al nombre del comando de transformación como una cadena Unicode.

</dd> <dt>

*pwszArg* \[ En\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero al argumento como una cadena Unicode.

</dd> <dt>

*pvarResult* \[ out, retval\]
</dt> <dd>

Tipo: **\* VARIANT**

Puntero a la variante de resultado. *pvarResult* no debe ser un **puntero NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**interfaz IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y Windows Server 2003, y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




