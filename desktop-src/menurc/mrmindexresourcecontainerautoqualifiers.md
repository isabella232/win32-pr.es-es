---
title: Función MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer. h)
description: Indexa los recursos de cadena incluidos en un archivo de recursos (. resw/. resjson) o un. priinfo o. prifile, que pertenece a una aplicación de UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menús de la función MrmIndexResourceContainerAutoQualifiers y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714611"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>MrmIndexResourceContainerAutoQualifiers función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Indexa los recursos de cadena incluidos en un archivo de recursos (. resw/. resjson) o un. priinfo o. prifile, que pertenece a una aplicación de UWP. Deduce una lista de calificadores de recursos del parámetro *containerPath* . Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ de\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indizador de recursos que indizará los recursos de cadena.

</dd> <dt>

*containerPath* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso relativa a un. resw,. resjson,. priinfo o. prifile que contiene los recursos de cadena que desea indizar. Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación de UWP para la que está generando archivos PRI. Esa raíz del proyecto es el valor de *projectRoot* que pasó a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="remarks"></a>Observaciones

Los calificadores de recursos se deducen de *containerPath*. Por ejemplo, un valor de L "en-US \\ \\ Resources. resw" agrega recursos de cadena con el calificador "Language-en-US".

El nombre del archivo de recursos se usará como el nombre del subárbol del mapa de recursos para estos recursos cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.

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

 

