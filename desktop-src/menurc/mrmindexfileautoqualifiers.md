---
title: Función MrmIndexFileAutoQualifiers (MrmResourceIndexer. h)
description: Indexa un archivo de recursos que pertenece a una aplicación de UWP. Deduce una lista de calificadores de recursos del parámetro filePath. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menús de la función MrmIndexFileAutoQualifiers y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149949"
---
# <a name="mrmindexfileautoqualifiers-function"></a>MrmIndexFileAutoQualifiers función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Indexa un archivo de recursos que pertenece a una aplicación de UWP. Deduce una lista de calificadores de recursos del parámetro *filePath* . Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ de\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indizador de recursos que indizará el archivo de recursos.

</dd> <dt>

*filePath* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso relativa a un archivo que contiene un recurso que desea indizar. Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación de UWP para la que está generando archivos PRI. Esa raíz del proyecto es el valor de *projectRoot* que pasó a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="remarks"></a>Observaciones

El segmento de nombre de archivo de *filePath* se usa como el nombre del recurso; y los calificadores de recursos se derivan de su ruta de acceso. Por ejemplo, si se pasa L "images \\ de-de \\ scale-100 \\background.png" a *filePath* , el indexador de recursos agrega un recurso denominado "background.png" con los calificadores de recursos "Language-de-de-de" y "Scale-100".

L "files" se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

