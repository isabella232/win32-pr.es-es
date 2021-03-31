---
title: Vincular a la DLL de acceso remoto
description: Si una aplicación se vincula estáticamente al archivo DLL de RASAPI32, la aplicación no se cargará si el servicio de acceso remoto no está instalado.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904734"
---
# <a name="linking-to-the-remote-access-dll"></a>Vincular a la DLL de acceso remoto

Si una aplicación se vincula estáticamente al archivo DLL de RASAPI32, la aplicación no se cargará si el servicio de acceso remoto no está instalado. Una aplicación RAS puede cargarse cuando no se instala RAS mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar el archivo dll y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener punteros a las funciones RAS.

Las funciones RAS se encuentran en RASAPI32.DLL. La biblioteca de importación para estas funciones es RASAPI32. Obj. Para usar las funciones RAS, los programas deben incluir los siguientes archivos:



| Archivo       | Descripción                                                                 |
|------------|-----------------------------------------------------------------------------|
| Acceso. C      | Contiene los prototipos de función RAS, las constantes y las definiciones de estructura. |
| RASERROR. C | Contiene los códigos de error de RAS.                                               |



 

 

 