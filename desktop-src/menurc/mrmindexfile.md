---
title: Función MrmIndexFile (MrmResourceIndexer. h)
description: Indexa un archivo de recursos que pertenece a una aplicación de UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menús de la función MrmIndexFile y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492538"
---
# <a name="mrmindexfile-function"></a>MrmIndexFile función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Indexa un archivo de recursos que pertenece a una aplicación de UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ de\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indizador de recursos que indizará el archivo de recursos.

</dd> <dt>

*resourceUri* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

URI de recurso que se va a asignar al recurso. La ruta de acceso se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.

</dd> <dt>

*filePath* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso relativa a un archivo que contiene un recurso que desea indizar. Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación de UWP para la que está generando archivos PRI. Esa raíz del proyecto es el valor de *projectRoot* que pasó a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> <dt>

*calificadores* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una lista opcional de calificadores de recursos, por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard". Una cadena vacía o **nullptr** indica un recurso neutro. Los calificadores de recursos *no* se deducen de *ResourceUri* ni de *containerPath*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="remarks"></a>Observaciones

Si desea especificar los calificadores de recursos, páselo en el parámetro *calificadores* . Los calificadores de recursos *no* se deducen de *ResourceUri* ni de *filePath*.

El segmento de nombre de archivo de *resourceUri* (no *filePath*) se usa como nombre del recurso.

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

 

