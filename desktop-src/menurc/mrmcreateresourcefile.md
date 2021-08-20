---
title: Función MrmCreateResourceFile (MrmResourceIndexer.h)
description: Crea un archivo PRI (denominado \ 0034;resources.pri \ 0034;) o archivos, en el disco de la carpeta especificada. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menús de función MrmCreateResourceFile y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58cd2ca366e2eeb4c594df986016d29c9aafbee0fa3310beded7a0b9bb12ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687338"
---
# <a name="mrmcreateresourcefile-function"></a>Función MrmCreateResourceFile

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Crea un archivo PRI (denominado "resources.pri") o archivos, en el disco de la carpeta especificada. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos desde el que se va a crear el archivo PRI.

</dd> <dt>

*packagingMode* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Especifica si el archivo PRI debe ser independiente, dividirse automáticamente por calificador de recursos o ser un paquete de recursos.

</dd> <dt>

*packagingOptions* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Especifica opciones adicionales sobre el archivo PRI.

</dd> <dt>

*Directorio_salida* 
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso a una carpeta en la que se va a guardar el archivo PRI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

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

 

