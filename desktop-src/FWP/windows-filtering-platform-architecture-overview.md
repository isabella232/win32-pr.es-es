---
title: Arquitectura de WFP
description: En esta sección se proporciona una breve introducción a la arquitectura de la plataforma de filtrado de Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271194"
---
# <a name="wfp-architecture"></a>Arquitectura de WFP

En la siguiente ilustración se muestra la arquitectura básica de la plataforma de filtrado de Windows (WFP).

![arquitectura básica del diagrama de la plataforma de filtrado de Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a>Motor de filtro

El motor de filtro contiene un componente de modo de usuario y un componente de modo kernel, que, en conjunto, realizan todas las operaciones de filtrado en los datos de red. El motor de filtro contiene varias capas de filtrado que se asignan de forma flexible a las capas de la pila de red del sistema operativo. Las capas del motor de filtros se dividen en capas en modo de usuario y en capas en modo kernel basadas en el componente del motor de filtro que las posee.

El componente de modo de usuario realiza el filtrado de RPC y IPsec. El motor de filtro contiene aproximadamente 10 niveles de filtrado de modo usuario.

El componente de modo kernel realiza el filtrado en los niveles de red y transporte de la pila TC/IP. Este componente también llama a las funciones de llamada disponibles durante el proceso de [clasificación](basic-operation.md) . El motor de filtro contiene aproximadamente 50 capas de filtrado de modo kernel.

Consulte [**filtrado de los identificadores de capas**](management-filtering-layer-identifiers-.md) para obtener una descripción de cada una de las capas del motor de filtro.

## <a name="base-filtering-engine"></a>Motor de filtrado de base

El motor de filtrado de base (BFE) es un servicio de modo de usuario (bfe.dll que se ejecuta en un proceso de svchost.exe) que coordina los componentes de WFP. Las tareas principales realizadas por BFE son la adición y eliminación de filtros del sistema, el almacenamiento de la configuración del filtro y la aplicación de la seguridad de configuración de WFP. Las aplicaciones se comunican con BFE a través de las [funciones de administración de WFP](fwp-mgmt-functions.md).

## <a name="callout-drivers"></a>Controladores de llamadas

Los controladores de llamadas proporcionan funcionalidad de filtrado adicional mediante la adición de funciones de llamada personalizadas al motor de filtro en uno o varios de los niveles de filtrado del modo kernel. Las llamadas admiten inspección profunda y paquetes, así como la modificación de secuencias. Una vez que un controlador de llamada ha agregado sus funciones de llamada al motor de filtro, los filtros que especifican la función de llamada de un controlador determinado se pueden agregar al proceso de filtrado. Estos filtros se pueden agregar mediante una aplicación de administración de modo de usuario o el propio controlador de llamada. La interfaz de modo kernel, proporcionada en el kit de desarrollo de Windows, solo se debe usar cuando sea necesario y no como sustituto de la API de modo de usuario.

> [!Note]  
> Para obtener más información sobre los controladores de llamadas, consulte la sección sobre la plataforma de filtrado de Windows del [Kit de desarrollo de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

La plataforma de filtrado de Windows incluye una serie de funciones de llamada integradas que se pueden usar para la comunicación de datos segura de IPsec, la configuración de filtrado con estado y el filtrado de modo oculto. Vea [**identificadores de llamada integrados**](built-in-callout-identifiers.md) para obtener una lista completa de funciones de llamada integradas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos](object-model.md)
</dt> <dt>

[Operación de WFP](basic-operation.md)
</dt> <dt>

[Controladores de llamadas de plataforma de filtrado de Windows: Guía de diseño](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Controladores de llamadas de plataforma de filtrado de Windows: referencia](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 