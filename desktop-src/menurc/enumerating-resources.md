---
title: Enumeración de recursos
description: En este tema se de abordan las funciones que se usan para obtener listas de recursos.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 6d3fbe60e3013fbeabdb21d74999040b51c42be2a1bb4521cda28a976bfe7aa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034343"
---
# <a name="enumerating-resources"></a>Enumeración de recursos

En determinadas situaciones, es posible que desee detectar el contenido de los recursos de un módulo portable ejecutable (PE) desconocido. El SDK Windows proporciona funciones de enumeración de recursos que permiten a la aplicación obtener listas de tipos de recursos, nombres e idiomas en un módulo especificado.

* Las [**funciones EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) y [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) proporcionan una lista de tipos de recursos que se encuentran en el módulo.
* Las [**funciones EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) y [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) proporcionan el nombre de cada recurso dentro de un tipo determinado.
* Las [**funciones EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) y [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) proporcionan el idioma de cada recurso de un nombre y tipo determinados. 

Estas funciones y sus funciones de devolución de llamada asociadas permiten a la aplicación crear una lista de todos los recursos de un módulo. Este proceso se describe en [Creación de una lista de recursos.](using-resources.md)

## <a name="-see-also"></a>-see-also

[Msistuff.exe aplicación de ejemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
