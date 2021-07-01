---
description: Obtenga información sobre las clases de C++ de WMI que forman parte del marco de proveedores WMI y que ahora se consideran en estado final.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Clases de marco de trabajo de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120450"
---
# <a name="provider-framework-classes"></a>Clases de marco de trabajo de proveedor

\[Las clases de C++ de WMI que forman parte del marco de proveedores WMI ahora se consideran en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El marco de trabajo del proveedor implementa las clases siguientes.



| Framework (clase)                                | Descripción                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contiene métodos para el procesamiento de consultas.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contiene métodos para establecer y recuperar propiedades y es una encapsulación de [**la interfaz IWbemClassObject.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) El implementador no debe tener que acceder directamente a **los métodos IWbemClassObject.** |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Clase base que proporciona los mecanismos de seguridad de subprocesos internos para el marco de proveedores WMI.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Parte del marco del proveedor WMI. Provider Framework implementa métodos de esta interfaz internamente para crear nuevas instancias de clases para el proveedor.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementa [**IWbemProviderInit y métodos**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) que controlan la carga y descarga del proveedor de marco.                                                                             |
| [**Proveedor**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contiene funciones auxiliares y proporciona implementaciones predeterminadas de los [**métodos de IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Tenga en cuenta que muchos de los métodos de marco [**usan parámetros CHString.**](chstring.md) **CHString** admite muchos de los mismos métodos y propiedades que Microsoft Foundation Classes (MFC), pero sin la sobrecarga de MFC. Para obtener más información sobre **CHString**, vea **Referencia de clase CHString**.

 

 
