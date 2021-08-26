---
title: Función MrmPeekResourceIndexerMessages (MrmResourceIndexer.h)
description: Ver los mensajes generados por un indexador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- Menús de la función MrmPeekResourceIndexerMessages y otros recursos
topic_type:
- apiref
api_name:
- MrmPeekResourceIndexerMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f72325ab147656873af2bbf13d7ce1cfa47802c816dc9f14f0c6ee4f3c821683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847335"
---
# <a name="mrmpeekresourceindexermessages-function"></a>Función MrmPeekResourceIndexerMessages

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Ver los mensajes generados por un indexador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmPeekResourceIndexerMessages(
  _In_  MrmResourceIndexerHandle  indexer,
  _Out_ MrmResourceIndexerMessage **messages,
  _Out_ ULONG                     *numMsgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos que desea ver los mensajes.

</dd> <dt>

*mensajes* \[ out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

Puntero a un puntero a [**mrmResourceIndexerMessage**](mrmresourceindexermessage.md). La función asigna una matriz de **MrmResourceIndexerMessage** y devuelve un puntero a esa memoria en *los mensajes*. No libera el puntero cuya dirección se pasa a los *mensajes*.

</dd> <dt>

*numMsgs* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Número de mensajes devueltos en *los mensajes*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

La aplicación no posee la memoria asignada y devuelta en los *mensajes,* por lo que no la libera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

