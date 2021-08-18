---
title: Vinculación a la DLL de acceso remoto
description: Si una aplicación se vincula estáticamente al archivo DLL RASAPI32, la aplicación no se cargará si el servicio de acceso remoto no está instalado.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b98757320cf9a166e741eb10ace8607d0287740a5494ca20fcc431b16b4367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790655"
---
# <a name="linking-to-the-remote-access-dll"></a>Vinculación a la DLL de acceso remoto

Si una aplicación se vincula estáticamente al archivo DLL RASAPI32, la aplicación no se cargará si el servicio de acceso remoto no está instalado. Una aplicación RAS se puede cargar cuando ras no está instalado mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar el archivo DLL y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener punteros a las funciones RAS.

Las funciones RAS se encuentran en RASAPI32.DLL. La biblioteca de importación de estas funciones es RASAPI32. Lib. Para usar las funciones RAS, los programas deben incluir los siguientes archivos:



| Archivo       | Descripción                                                                 |
|------------|-----------------------------------------------------------------------------|
| Ras. H      | Contiene los prototipos de función RAS, constantes y definiciones de estructura. |
| RASERROR. H | Contiene los códigos de error ras.                                               |



 

 

 