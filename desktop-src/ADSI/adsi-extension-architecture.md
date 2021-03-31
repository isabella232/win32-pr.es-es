---
title: Arquitectura de extensión ADSI
description: Las extensiones ADSI se basan en el modelo de agregación COM con varias mejoras. Las extensiones deben cumplir todas las reglas de COM. Para obtener más información, vea la especificación COM.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, arquitectura de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377409f4b9ac36d72d6885e89860b9e6e680b103
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793864"
---
# <a name="adsi-extension-architecture"></a>Arquitectura de extensión ADSI

Las extensiones ADSI se basan en el modelo de agregación COM con varias mejoras. Las extensiones deben cumplir todas las reglas de COM. Para obtener más información, vea la especificación COM.

Esta es una revisión del modelo de agregación COM.

![modelo de agregación com](images/comagmod.png)

Un agregado, también conocido como objeto interno, es un objeto que crea un agregador. El objeto de extensión es un agregado.

Un agregador, también conocido como objeto externo, es un objeto que crea un agregado. ADSI es un agregador.

El objeto interno delega su [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en el **IUnknown** del agregador.

Las extensiones ADSI agregan las siguientes mejoras a la agregación COM para satisfacer sus requisitos:

-   Permite a cada escritor de extensiones extender los objetos ADSI. Un escritor de extensiones puede registrar su extensión con ADSI y no verse afectada por la existencia de otras extensiones. En el modelo de agregación COM, el agregador debe tener el CLSID del agregado. ADSI reduce este requisito haciéndolo actuar como agregador para todas las extensiones. Por lo tanto, en lugar de formar una capa de componentes anidados, las extensiones se encuentran en el mismo nivel.
-   Permite un objeto, uno IDispatch. La compatibilidad con la automatización es una de las características más importantes de ADSI. La compatibilidad con la automatización se consigue porque ADSI es compatible con la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Se recomienda a los escritores de extensiones que admitan la interfaz **IDispatch** . Sin embargo, solo debería haber una interfaz **IDispatch** en un objeto determinado. ADSI integra y recopila las muchas interfaces **IDispatch** de extensiones diferentes y las presenta como una **IDispatch** coherente en el controlador de Automation. Cada extensión, cuando se agrega, debe volver a enrutar sus llamadas **IDispatch** a la **IDISPATCH** proporcionada por ADSI.

Todas estas soluciones son posibles debido a los servicios que proporciona el administrador de objetos ADSI, que residen en cada proveedor ADSI.

En la siguiente ilustración se muestra la arquitectura del modelo de extensión ADSI.

![arquitectura del modelo de extensión ADSI](images/adsiexmo.png)

ADSI admite dos niveles de extensión:

-   Compatibilidad con enlaces tempranas. Este es el primer nivel de extensión. Una extensión debe admitir el registro e implementar nuevas interfaces. Los consumidores de la extensión deben usar herramientas o hosts de scripting que admitan el enlace en tiempo de compilación, por ejemplo, Visual C++ Visual Basic.
-   Compatibilidad con enlace en tiempo de ejecución. Esto sucede cuando una extensión cumple todos los requisitos de enlace temprano e implementa una interfaz adicional, [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Los implementadores de extensión pueden utilizar cualquier herramienta que funcione como controlador de automatización, como Windows Script Host, páginas de Active Server o HTML con VBScript.

 

 