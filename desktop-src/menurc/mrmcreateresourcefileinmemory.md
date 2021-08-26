---
title: Función MrmCreateResourceFileInMemory (MrmResourceIndexer.h)
description: Crea información de PRI como un blob en memoria, no como un archivo en el disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menús de la función MrmCreateResourceFileInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff34ddaab25f47f537c1270ad3a70719a43e2e1efa978fbad19cbe9ae77ba937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886755"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>Función MrmCreateResourceFileInMemory

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Crea información de PRI como un blob en memoria, no como un archivo en el disco. La función asigna memoria y devuelve un puntero a esa memoria en *outputPriData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos a partir del cual se va a crear la información del PRI.

</dd> <dt>

*packagingMode* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Especifica si la información de PRI debe ser independiente o ser un paquete de recursos. **No se admite MrmPackagingModeAutoSplit.**

</dd> <dt>

*packagingOptions* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Especifica opciones adicionales sobre la información de PRI.

</dd> <dt>

*outputPriData* \[ out\]
</dt> <dd>

Tipo: **\* \* BYTE**

Dirección de un puntero a BYTE. La función asigna memoria y devuelve un puntero a esa memoria en *outputPriData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el puntero a BYTE para liberar esa memoria.

</dd> <dt>

*outputPriSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Dirección de un ULONG. En *outputPriSize*, la función devuelve el tamaño de la memoria asignada a la que *apunta outputPriData.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

Si pasa *outputPriData* a [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), no liberará la memoria hasta que haya terminado de usar el indexador de recursos.

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

 

