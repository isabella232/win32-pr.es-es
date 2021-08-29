---
description: Hay dos métodos por los que una aplicación de hospedaje puede buscar ensamblados en paralelo.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Buscar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d5ffe20d7453581bd76e8d2e737fde6cab5f470d22b516c6fc28a7182e9382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141928"
---
# <a name="searching-for-assemblies"></a>Buscar ensamblados

Hay dos métodos por los que una aplicación de hospedaje puede buscar ensamblados en paralelo.

Los módulos hospedados pueden registrarse con la aplicación de hospedaje ampliando cierta información de configuración compartida. A continuación, la aplicación puede usar esta información de configuración para cargar los ensamblados necesarios para la nueva funcionalidad. Para ello, se puede llamar a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) en los manifiestos especificados en los datos de registro, seguido de llamar a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para entrar en el nuevo módulo. Tenga en cuenta que con este método, los nuevos componentes tienen que actualizar algún estado de aplicación compartido para indicar su presencia.

La aplicación de hospedaje puede buscar activamente los ensamblados al iniciarse mediante [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para buscar archivos DLL o manifiestos en una ubicación especificada y, a continuación, usar [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) para acceder a la información. Este método no requiere ningún registro del componente.

 

 
