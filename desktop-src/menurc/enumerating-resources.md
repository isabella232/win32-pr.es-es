---
title: Enumerar recursos
description: En este tema se describen las funciones que se usan para obtener listas de recursos.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ea7f2600f6da98cff6f16853092004a542b0f206
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105653297"
---
# <a name="enumerating-resources"></a>Enumerar recursos

En determinadas situaciones, puede que desee detectar el contenido de los recursos de un módulo ejecutable portable (PE) desconocido. El Windows SDK proporciona funciones de enumeración de recursos que permiten a la aplicación obtener listas de tipos de recursos, nombres y lenguajes en un módulo especificado.

* Las funciones [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) y [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) proporcionan una lista de los tipos de recursos que se encuentran en el módulo.
* Las funciones [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) y [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) proporcionan el nombre de cada recurso dentro de un tipo determinado.
* Las funciones [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) y [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) proporcionan el idioma de cada recurso de un nombre y tipo determinados. 

Estas funciones y sus funciones de devolución de llamada asociadas permiten a la aplicación crear una lista de todos los recursos de un módulo. Este proceso se describe en [creación de una lista de recursos](using-resources.md).

## <a name="-see-also"></a>-véase: también

[Msistuff.exe aplicación de ejemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
