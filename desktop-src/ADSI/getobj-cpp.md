---
title: GETOBJ. Cpp
description: En el componente de proveedor de ejemplo, aparece un ejemplo de código que se usa para buscar y enlazar objetos en Getobj.cpp. Las rutinas admitidas se enumeran en la tabla siguiente.
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1bada2480c8d361ba6dc1b71928aa6d1a1f945c75e0202312cc7f3e34c97b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082579"
---
# <a name="getobjcpp"></a>GETOBJ. Cpp

En el componente de proveedor de ejemplo, aparece un ejemplo de código que se usa para buscar y enlazar objetos en Getobj.cpp. Las rutinas admitidas se enumeran en la tabla siguiente.



| Elemento                                | Descripción                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RelativeGetObject**               | Obtiene un objeto relativo a un ADsPath determinado.                                                                                                                                                                                                                                                       |
| **Getobject**                       | Llama **a ADsObject** (Parse.cpp) para comprobar la sintaxis de la ruta de acceso, valida que la ruta de acceso tiene el token de proveedor correcto y valida el tipo de objeto. Si no existe ningún error, cree una instancia del tipo correcto de objeto y recupere un puntero a la interfaz [**IUnknown del**](/windows/win32/api/unknwn/nn-unknwn-iunknown) objeto. |
| **BuildADsPathFromDSPath**          | Se ha creado una cadena ADsPath a partir de la ruta de acceso del directorio nativo.                                                                                                                                                                                                                                           |
| **BuildDSTreeNameFromADsPath**      | Use ADsPath para crear una posible ruta de acceso del directorio de árbol para la ruta de acceso del directorio nativo.                                                                                                                                                                                                           |
| **BuildDSPathFromADsPath**          | Usa ADsPath y DSPathName.                                                                                                                                                                                                                                                                      |
| **BuildADsParentPath**              | Compile ADsPath en el elemento primario para este objeto.                                                                                                                                                                                                                                                  |
| **GetNamespaceObject**              | Valide y [**CoCreateInstance un**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) objeto de espacio de nombres de ejemplo.                                                                                                                                                                                                           |
| **ValidateNamespaceObject**         | Compruebe que el objeto de espacio de nombres coincide con el nombre del proveedor actual.                                                                                                                                                                                                                               |
| **ValidateProvider**                | Valide el nombre del proveedor (distingue mayúsculas de minúsculas).                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | Valide y abra el tipo de objeto de esquema adecuado. A continuación, cree el correcto y recupere el puntero de interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en él.                                                                                                                                        |
| **ValidateSchemaObject**            | Compruebe que es un tipo de objeto de esquema válido.                                                                                                                                                                                                                                                     |
| **ValidateObjectType**              | Compruebe que el tipo de objeto existe en el esquema.                                                                                                                                                                                                                                                 |
| **BuildSampleDSRootRDNFromADsPath** | Compile ADsPath en el nodo raíz para el componente de proveedor de ejemplo.                                                                                                                                                                                                                            |
| **BuildDSPathFromADsPath**          | Usa ADsPath, DSRootRDN y DSPathName.                                                                                                                                                                                                                                                          |



 

 

 