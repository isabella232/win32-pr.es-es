---
title: Arquitectura de extensión ADSI
description: Las extensiones ADSI se basan en el modelo de agregación COM con varias mejoras. Las extensiones deben cumplir todas las reglas COM. Para más información, consulte la especificación COM.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, arquitectura de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239a2562054f062464fc924a0f67c31ea3d9fab696fd23e532eab78e1dc66d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023882"
---
# <a name="adsi-extension-architecture"></a>Arquitectura de extensión ADSI

Las extensiones ADSI se basan en el modelo de agregación COM con varias mejoras. Las extensiones deben cumplir todas las reglas COM. Para más información, consulte la especificación COM.

Esta es una revisión del modelo de agregación COM.

![modelo de agregación com](images/comagmod.png)

Un agregado, también conocido como objeto interno, es un objeto que crea un agregador. El objeto de extensión es un agregado.

Un agregador, también conocido como objeto externo, es un objeto que crea un agregado. ADSI es un agregador.

El objeto interno delega su [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en el **IUnknown del agregador.**

Las extensiones ADSI agregan las siguientes mejoras a la agregación COM para satisfacer sus requisitos:

-   Permite que cada escritor de extensiones extienda objetos ADSI. Un escritor de extensiones puede registrar su extensión con ADSI y no verse afectado por la existencia de otras extensiones. En el modelo de agregación COM, el agregador debe tener el CLSID del agregado. ADSI relaja este requisito haciendo que actúe como agregador para todas las extensiones. Por lo tanto, en lugar de formar una capa de componentes anidados, las extensiones están en el mismo nivel.
-   Permite un objeto, un IDispatch. La compatibilidad con automatización es una de las características más importantes de ADSI. La compatibilidad con Automatización se logra porque ADSI admite la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Se recomienda a los escritores de extensiones que admitan **la interfaz IDispatch.** Sin embargo, solo debe haber una **interfaz IDispatch** en un objeto determinado. ADSI integra y recopila las muchas interfaces **IDispatch** de diferentes extensiones y las presenta como un **IDispatch** coherente al controlador de Automation. Cada extensión, cuando se agrega, debe volver a enrutar sus llamadas **IDispatch** a **la IDispatch** proporcionada por ADSI.

Todas estas soluciones son posibles debido a los servicios que proporciona el Administrador de objetos ADSI, que residen en cada proveedor adsi.

En la ilustración siguiente se muestra la arquitectura del modelo de extensión ADSI.

![Arquitectura del modelo de extensión adsi](images/adsiexmo.png)

ADSI admite dos niveles de extensión:

-   Compatibilidad con enlaces anticipados. Este es el primer nivel de extensión. Una extensión debe admitir el registro e implementar nuevas interfaces. Los consumidores de extensiones deben usar herramientas o hosts de scripting que admitan el enlace temprano, por ejemplo, Visual C++ , Visual Basic.
-   Compatibilidad con enlaces en tiempo de tarde. Esto sucede cuando una extensión cumple todos los requisitos de enlace iniciales e implementa una interfaz adicional, [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Los implementadores de extensiones pueden usar cualquier herramienta que funcione como controlador de Automation, como el host de script de Windows, Active Server Pages o HTML con VBScript.

 

 