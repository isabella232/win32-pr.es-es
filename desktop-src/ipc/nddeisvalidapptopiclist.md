---
description: Determina si una aplicación y una cadena de tema (&\# 0034; AppName \| TopicName&\# 0034;) usa la sintaxis adecuada.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Función NDdeIsValidAppTopicList (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172290"
---
# <a name="nddeisvalidapptopiclist-function"></a>Función NDdeIsValidAppTopicList

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Determina si una aplicación y una cadena de tema ("*AppName* \| *TopicName*") usa la sintaxis adecuada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*targetTopic* \[ En\]
</dt> <dd>

Puntero a la aplicación y cadena de tema que se validará. Este parámetro no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el *parámetro targetTopic* tiene una sintaxis válida, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

[**NDdeShareAdd**](nddeshareadd.md) también llama a esta función cuando crea el recurso compartido de DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Nombres Unicode y ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) y **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




