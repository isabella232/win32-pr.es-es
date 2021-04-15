---
title: Almacenamiento asincrónico
description: El almacenamiento asincrónico mejora la especificación de almacenamiento estructurado COM para admitir la descarga asincrónica de objetos de almacenamiento en redes de alta latencia y vínculo de baja velocidad, como Internet.
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- Almacenamiento estructurado Strctd STG, almacenamiento asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488059"
---
# <a name="asynchronous-storage"></a>Almacenamiento asincrónico

El almacenamiento asincrónico mejora la especificación de almacenamiento estructurado COM para admitir la descarga asincrónica de objetos de almacenamiento en redes de alta latencia y vínculo de baja velocidad, como Internet. El almacenamiento asincrónico permite que las aplicaciones nuevas y heredadas que usan archivos compuestos representen eficazmente su contenido cuando se obtiene acceso a ellos a través de los protocolos de Internet existentes. Una única solicitud a un servidor de World Wide Web desencadena la descarga de objetos anidados contenidos en una página web, lo que elimina la necesidad de solicitar por separado cada objeto. Un mecanismo de descarga y acceso asincrónico permite a una aplicación representar la primera página de datos antes de que se hayan recibido todos los datos. El editor web puede especificar el orden exacto en el que los elementos de una página están disponibles y no depende de factores aleatorios de la topología de red y la disponibilidad del servidor.

El almacenamiento asincrónico funciona junto con monikers asincrónicos para proporcionar un comportamiento de enlace asincrónico completo. Para obtener más información acerca de los monikers asincrónicos, vea el kit de desarrollo de software de Microsoft ActiveX. Un moniker asincrónico específico del protocolo desencadena la operación de enlace y configura los componentes necesarios. En el caso de Internet, este moniker sería uno que puede analizar una dirección URL para enlazar a un objeto o almacenamiento. Si el destino de la operación de enlace es un objeto persistente, la llamada a [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) devuelve un objeto de almacenamiento asincrónico.

> [!Note]  
> La versión actual de los monikers de la dirección URL de Microsoft no admite el almacenamiento asincrónico.

 

Un cliente de moniker asincrónico solicita el enlace asincrónico implementando un objeto de devolución de llamada de estado de enlace y registrándose con el contexto de enlace. El objeto de devolución de llamada de estado de enlace expone la interfaz [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) , que permite al cliente especificar preferencias de enlace y recibir notificaciones de disponibilidad de datos globales y de progreso durante el transcurso de una operación de enlace. La implementación de archivo compuesto asincrónico proporciona un punto de conexión para [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify), que los clientes pueden usar para recibir notificaciones de disponibilidad específicas en flujos individuales.

 

 