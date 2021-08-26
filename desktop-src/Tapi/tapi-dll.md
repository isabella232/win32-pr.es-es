---
description: Los archivos DLL de TAPI, junto con el servidor TAPI (Tapisvr.exe), son abstracciones fundamentales que separan las aplicaciones de usuario final o servidor de los proveedores de servicios. Un archivo DLL de TAPI junto con el servidor TAPI proporciona una interfaz coherente entre estas dos capas.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff26274baf25047212a3f9f8e15c2211d90cbaa10db23674ae54dbb97bbfdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012214"
---
# <a name="tapi-dll"></a>TAPI DLL

Los archivos DLL de TAPI, junto con el servidor TAPI (Tapisvr.exe), son abstracciones fundamentales que separan las aplicaciones de usuario final o servidor de los proveedores de servicios. Un archivo DLL de TAPI junto con el servidor TAPI proporciona una interfaz coherente entre estas dos capas.

Una aplicación TAPI carga el archivo DLL adecuado en su espacio de proceso. Durante la inicialización, TAPI establece un vínculo RPC con Tapisvr.exe. El servidor TAPI se ejecuta en el contexto de SVCHOST.

Hay tres archivos DLL asociados a TAPI: Tapi.dll, Tapi32.dll y Tapi3.dll. Estos archivos DLL se encuentran en %SystemRoot% \\ system32. En la ilustración siguiente se muestran los roles de sus respectivos roles en Telefonía de Microsoft:

![roles de los tres archivos DLL de tapi](images/dllserv.png)

Las aplicaciones de 16 bits existentes se vinculan a Tapi.dll. Tapi.dll es simplemente una capa thunk que asigna direcciones de 16 bits a direcciones de 32 bits y pasa solicitudes a Tapi32.dll.

Las aplicaciones TAPI 2.x de 32 bits existentes se vinculan a Tapi32.dll. Tapi32.dll es una capa de marshalling fino que transfiere las solicitudes de función al servidor TAPI (TAPISRV) y, cuando es necesario, carga e invoca archivos DLL del proveedor de servicios multimedia en el proceso de la aplicación.

Las aplicaciones TAPI 3.x vinculan a Tapi3.dll.

 

 



