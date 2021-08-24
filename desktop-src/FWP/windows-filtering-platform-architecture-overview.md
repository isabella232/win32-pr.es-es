---
title: Arquitectura de WFP
description: En esta sección se proporciona una breve introducción a la arquitectura de Windows de filtrado.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41989a11ff5412b3185f6987f9588f0309c3fde3ca386c71e4613ab6bc8237f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766614"
---
# <a name="wfp-architecture"></a>Arquitectura de WFP

En la ilustración siguiente se muestra la arquitectura básica de la plataforma Windows filtrado de datos (WFP).

![arquitectura básica del diagrama de la plataforma de filtrado de ventanas](images/wfp-architecture.png)

## <a name="filter-engine"></a>Motor de filtros

El motor de filtro contiene un componente de modo de usuario y un componente de modo kernel, que juntos realizan todas las operaciones de filtrado en los datos de red. El motor de filtro contiene varias capas de filtrado que se asignan de forma flexible a las capas de pila de red del sistema operativo. Las capas del motor de filtro se dividen en capas de modo de usuario y capas de modo kernel en función del componente del motor de filtro que las posee.

El componente de modo de usuario realiza el filtrado rpc e IPsec. El motor de filtros contiene aproximadamente 10 capas de filtrado en modo de usuario.

El componente de modo kernel realiza el filtrado en las capas de red y transporte de la pila DE TC/IP. Este componente también llama a las funciones de llamada disponibles durante el proceso [de](basic-operation.md) clasificación. El motor de filtro contiene aproximadamente 50 capas de filtrado en modo kernel.

Consulte [**Filtrado de identificadores de capa**](management-filtering-layer-identifiers-.md) para obtener una descripción de cada una de las capas del motor de filtro.

## <a name="base-filtering-engine"></a>Motor de filtrado de base

El motor de filtrado base (BFE) es un servicio en modo de usuario (bfe.dll se ejecuta en un proceso svchost.exe) que coordina los componentes de WFP. Las tareas principales que realiza BFE son agregar y quitar filtros del sistema, almacenar la configuración de filtro y aplicar la seguridad de configuración de WFP. Las aplicaciones se comunican con BFE a través de [las funciones de administración de WFP](fwp-mgmt-functions.md).

## <a name="callout-drivers"></a>Controladores de llamada

Los controladores de llamada proporcionan funcionalidad de filtrado adicional mediante la adición de funciones de llamada personalizadas al motor de filtro en una o varias de las capas de filtrado en modo kernel. Las llamadas admiten la inspección en profundidad y el paquete, así como la modificación de secuencias. Una vez que un controlador de llamada ha agregado sus funciones de llamada al motor de filtro, los filtros que especifican la función de llamada de un controlador determinado se pueden agregar al proceso de filtrado. Estos filtros se pueden agregar mediante una aplicación de administración en modo de usuario o por el propio controlador de llamada. La interfaz de modo kernel, que se entrega en el kit de desarrollo de Windows, solo debe usarse cuando sea necesario y no como sustituto de la API en modo de usuario.

> [!Note]  
> Para obtener más información sobre los controladores de llamada, vea la Windows filtering platform del kit [de Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

La Windows filtrado de datos incluye una serie de funciones de llamada integradas que se pueden usar para la comunicación segura de datos de IPsec, la configuración de filtrado con estado y el filtrado en modo sigiloso. Consulte [**Identificadores de llamada integrados**](built-in-callout-identifiers.md) para obtener una lista completa de las funciones de llamada integradas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos](object-model.md)
</dt> <dt>

[Operación WFP](basic-operation.md)
</dt> <dt>

[Windows Filtrado de controladores de llamada de plataforma: Guía de diseño](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Windows Filtrar controladores de llamada de plataforma: referencia](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 