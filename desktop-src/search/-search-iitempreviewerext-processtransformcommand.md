---
description: Permite el procesamiento de un comando de transformación que se encuentra en una plantilla de vista previa.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt::P método rocessTransformCommand
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
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907752"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt::P método rocessTransformCommand

Permite el procesamiento de un comando de transformación que se encuentra en una plantilla de vista previa.

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

*dwContext* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto para la operación. Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.

</dd> <dt>

*pwszName* \[ de\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero al nombre del comando de transformación como una cadena Unicode.

</dd> <dt>

*pwszArg* \[ de\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero al argumento como una cadena Unicode.

</dd> <dt>

*pvarResult* \[ out, retval\]
</dt> <dd>

Tipo: **variante \** _

Puntero a la variante de resultado. _pvarResult * no debe ser un puntero **nulo** .

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

 

 




