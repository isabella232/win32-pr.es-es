---
description: En este tema se describe cómo crear un experto genérico que se incluye con Monitor de red SDK.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Creación de un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071569"
---
# <a name="building-an-expert"></a>Creación de un experto

En este tema se describe cómo crear un experto genérico que se incluye con Monitor de red SDK.

> [!Note]  
> Antes de crear los siguientes ejemplos de código, instale Monitor de red SDK e inicialice el MySetEnv.bat archivo.

 

**Para crear un experto genérico**

1.  Abra un Monitor de red de comandos y vaya al subdirectorio Expertos; por ejemplo, C: Archivos de programa \\ \\ \\ NetMonSDK2 \\ Experts.
2.  Escriba **xcopy /e /s /v Blrplate MyEfactor**; a continuación, cuando se le solicite, **escriba D**.
3.  Mueva al \\ subdirectorio MyE subcarpeta.
4.  Escriba **ren Blrplate \* . \* MyExpert \* \* .** Asegúrese de que se ha cambiado el nombre de todos los archivos correctamente. Compruebe los nombres de archivo comparando los archivos en el \\ subdirectorio Experts \\ Blrplate.
5.  Edite el archivo Make reemplazando todas las apariciones de **Blrplate** por **MyEfactor**.
6.  Edite ambos archivos .cpp reemplazando todas las apariciones de **Blrplate** por **MyEfactor**. Tenga en cuenta que el identificador del cuadro de diálogo de Config.cpp debe estar en mayúsculas (por ejemplo, **MYEGNI).**
7.  Edite MyEfactor.h reemplazando todas las apariciones de **Blrplate** por **MyEfactor**.
8.  Edite Resrc1.h mediante el cambio de nombre **de BLRPLATE** a **MYEFACTOR.** (Recuerde que **MYEVOLUCION** debe estar en mayúsculas).
9.  Edite el archivo MyEfactor.rc mediante el cambio de nombre **IDD \_ BLRPLATE \_ CONFIG \_ DIALOG** a **IDD \_ MYEFACTOR \_ CONFIG \_ DIALOG**.
10. Escriba **nmake para** compilar el archivo DLL. Para comprobar la compilación, cambie el directorio al \\ subdirectorio Obj y compruebe que el archivo existe. Para obtener más información, vea [Ver las propiedades de DLL expertos.](viewing-expert-dll-properties.md)

Una vez completada la compilación, tendrá un archivo DLL experto que puede probar e implementar con Monitor de red. Para obtener más información sobre la instalación de un experto, vea [Installing an Expert to Monitor de red 2.1](installing-an-expert-to-network-monitor-2-1.md). Para obtener más información sobre la depuración de un experto, vea [Depuración de un experto.](debugging-an-expert.md)

 

 



