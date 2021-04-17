---
description: Los archivos dll de TAPI, junto con el servidor TAPI (Tapisvr.exe), son abstracciones cruciales que separan las aplicaciones de usuario final o de servidor de los proveedores de servicios. Una DLL de TAPI junto con el servidor TAPI proporciona una interfaz coherente entre estas dos capas.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL DE TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560217"
---
# <a name="tapi-dll"></a>DLL DE TAPI

Los archivos dll de TAPI, junto con el servidor TAPI (Tapisvr.exe), son abstracciones cruciales que separan las aplicaciones de usuario final o de servidor de los proveedores de servicios. Una DLL de TAPI junto con el servidor TAPI proporciona una interfaz coherente entre estas dos capas.

Una aplicación TAPI carga el archivo DLL adecuado en su espacio de proceso. Durante la inicialización, TAPI establece un vínculo RPC con Tapisvr.exe. El servidor TAPI se ejecuta en el contexto de SVCHOST.

Hay tres dll asociadas a TAPI: Tapi.dll, Tapi32.dll y Tapi3.dll. Estos archivos DLL se encuentran en% SystemRoot% \\ system32. En la ilustración siguiente se muestran los roles de sus respectivos roles en telefonía de Microsoft:

![roles de los tres archivos dll de TAPI](images/dllserv.png)

Las aplicaciones de 16 bits existentes se vinculan a Tapi.dll. Tapi.dll es simplemente una capa de código thunk que asigna direcciones de 16 bits a direcciones de 32 bits y solicitudes de paso a Tapi32.dll.

Las aplicaciones TAPI 2. x de 32 bits existentes se vinculan a Tapi32.dll. Tapi32.dll es una capa de serialización fina que transfiere las solicitudes de función al servidor TAPI (TAPISRV) y, cuando sea necesario, carga e invoca los archivos DLL del proveedor de servicios multimedia en el proceso de la aplicación.

Las aplicaciones TAPI 3. x se vinculan a Tapi3.dll.

 

 



