---
description: Hay dos métodos por los que una aplicación de hospedaje puede buscar ensamblados en paralelo.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Buscar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649193"
---
# <a name="searching-for-assemblies"></a>Buscar ensamblados

Hay dos métodos por los que una aplicación de hospedaje puede buscar ensamblados en paralelo.

Los módulos hospedados pueden registrarse en la aplicación de hospedaje extendiendo parte de la información de configuración compartida. A continuación, la aplicación puede usar esta información de configuración para cargar los ensamblados necesarios para la nueva funcionalidad. Esto se puede hacer llamando a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) en los manifiestos especificados en los datos de registro, seguido de una llamada a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para entrar en el nuevo módulo. Tenga en cuenta que, con este método, los nuevos componentes deben actualizar el estado de la aplicación compartida para indicar su presencia.

La aplicación de hospedaje puede buscar activamente los ensamblados al inicio mediante [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para buscar archivos dll o manifiestos en una ubicación especificada y, a continuación, usar [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) para tener acceso a la información. Este método no requiere ningún registro del componente.

 

 
