---
description: Determina si una aplicación y una cadena de tema (&\# 0034; AppName \| TopicName&\# 0034;) usa la sintaxis correcta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Función NDdeIsValidAppTopicList (Nddeapi. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688393"
---
# <a name="nddeisvalidapptopiclist-function"></a>NDdeIsValidAppTopicList función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Determina si una aplicación y una cadena de tema ("*appname* \| *TopicName*") utiliza la sintaxis correcta.

## <a name="syntax"></a>Sintaxis


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*targetTopic* \[ de\]
</dt> <dd>

Un puntero a la aplicación y la cadena de tema que se va a validar. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el parámetro *targetTopic* tiene una sintaxis válida, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

[**NDdeShareAdd**](nddeshareadd.md) también llama a esta función cuando crea el recurso compartido DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Nombres Unicode y ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) y **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




