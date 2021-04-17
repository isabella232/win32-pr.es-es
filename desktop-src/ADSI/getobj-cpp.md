---
title: GETOBJ. CPP
description: En el componente proveedor de ejemplo, aparece un ejemplo de código que se usa para buscar y enlazar objetos en Getobj. cpp. En la tabla siguiente se enumeran las rutinas admitidas.
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d58647208c68437c068d58cd9908bc08989141
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359416"
---
# <a name="getobjcpp"></a>GETOBJ. CPP

En el componente proveedor de ejemplo, aparece un ejemplo de código que se usa para buscar y enlazar objetos en Getobj. cpp. En la tabla siguiente se enumeran las rutinas admitidas.



| Elemento                                | Descripción                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RelativeGetObject**               | Obtiene un objeto relativo a un ADsPath determinado.                                                                                                                                                                                                                                                       |
| **GetObject**                       | Llama a **ADsObject** (Parse. cpp) para comprobar la sintaxis de la ruta de acceso, valida que la ruta de acceso tiene el token del proveedor correcto y valida el tipo de objeto. Si no existe ningún error, cree una instancia del tipo correcto de objeto y recupere un puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del objeto. |
| **BuildADsPathFromDSPath**          | Generó una cadena ADsPath desde la ruta de acceso del directorio nativo.                                                                                                                                                                                                                                           |
| **BuildDSTreeNameFromADsPath**      | Use el ADsPath para crear una posible ruta de acceso al directorio de árbol para la ruta de acceso del directorio nativo.                                                                                                                                                                                                           |
| **BuildDSPathFromADsPath**          | Usa ADsPath y DSPathName.                                                                                                                                                                                                                                                                      |
| **BuildADsParentPath**              | Compile el ADsPath en el elemento primario de este objeto.                                                                                                                                                                                                                                                  |
| **GetNamespaceObject**              | Valide e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) un objeto de espacio de nombres de ejemplo.                                                                                                                                                                                                           |
| **ValidateNamespaceObject**         | Compruebe que el objeto de espacio de nombres coincide con el nombre del proveedor actual.                                                                                                                                                                                                                               |
| **ValidateProvider**                | Valida el nombre del proveedor (distingue mayúsculas de minúsculas).                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | Valide y abra el tipo de objeto de esquema adecuado. A continuación, cree la correcta y recupere el puntero de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en ella.                                                                                                                                        |
| **ValidateSchemaObject**            | Compruebe que es un tipo de objeto de esquema válido.                                                                                                                                                                                                                                                     |
| **ValidateObjectType**              | Compruebe que el tipo de objeto existe en el esquema.                                                                                                                                                                                                                                                 |
| **BuildSampleDSRootRDNFromADsPath** | Compile el ADsPath en el nodo raíz para el componente de proveedor de ejemplo.                                                                                                                                                                                                                            |
| **BuildDSPathFromADsPath**          | Usa ADsPath, DSRootRDN y DSPathName.                                                                                                                                                                                                                                                          |



 

 

 