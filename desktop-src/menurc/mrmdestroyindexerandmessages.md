---
title: Función MrmDestroyIndexerAndMessages (MrmResourceIndexer.h)
description: Libera los recursos de la máquina asociados a un indexador de recursos.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Menús y otros recursos de la función MrmDestroyIndexerAndMessages
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16dd8c03fdf4b89f734cf45c5ede0d2a55d377fae52e1a52139f82a0dcdf654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733665"
---
# <a name="mrmdestroyindexerandmessages-function"></a>Función MrmDestroyIndexerAndMessages

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información aquí proporcionada.\]

Libera los recursos de la máquina asociados a un indexador de recursos. Destruye el identificador, libera el indexador y elimina los mensajes. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de [paquetes (PRI) y sistemas de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos que se destruirá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

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

 

