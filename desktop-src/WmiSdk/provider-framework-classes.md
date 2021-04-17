---
description: Las clases de C++ de WMI que forman parte del marco de trabajo del proveedor de WMI ahora se consideran en estado final.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Clases de Framework de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1562d00e6b3b1563ece933ba7dd9361dd8a5d94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716202"
---
# <a name="provider-framework-classes"></a>Clases de Framework de proveedor

\[Las clases de C++ de WMI que forman parte del marco de trabajo del proveedor de WMI ahora se consideran en estado final y no estarán disponibles más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El marco de trabajo del proveedor implementa las siguientes clases.



| Clase de marco                                | Descripción                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contiene métodos para el procesamiento de consultas.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contiene métodos para establecer y recuperar propiedades y es una encapsulación de la interfaz [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) . El implementador no debe tener acceso directamente a los métodos **IWbemClassObject** . |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Una clase base que proporciona los mecanismos de seguridad de subprocesos internos para el marco de trabajo del proveedor WMI.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Parte del marco de trabajo del proveedor WMI. El marco de trabajo del proveedor implementa los métodos de esta interfaz internamente para crear nuevas instancias de clases para el proveedor.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implementa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y métodos que controlan la carga y descarga del proveedor de .NET Framework.                                                                             |
| [**Proveedor**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contiene funciones auxiliares y proporciona implementaciones predeterminadas de los métodos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Tenga en cuenta que muchos de los métodos de Framework usan los parámetros [**CHString**](chstring.md) . **CHString** admite muchos de los mismos métodos y propiedades que el Microsoft Foundation Classes (MFC), pero sin la sobrecarga de MFC. Para obtener más información sobre **CHString**, consulte referencia de la **clase CHString**.

 

 
