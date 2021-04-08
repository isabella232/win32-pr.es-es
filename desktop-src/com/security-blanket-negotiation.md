---
title: Negociación de la capa de seguridad
description: Negociación de la capa de seguridad
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078443"
---
# <a name="security-blanket-negotiation"></a>Negociación de la capa de seguridad

Una capa de seguridad es un grupo de valores que describen la configuración de seguridad que se aplica a todos los servidores proxy de un proceso o solo a un proxy de interfaz determinado. Un marco de seguridad consta de los siguientes valores:

-   Servicio de autenticación
-   Servicio de autorización
-   Nombre principal
-   Nivel de autenticación
-   Nivel de suplantación
-   Identidad de autenticación
-   Funcionalidades
-   Una lista de control de acceso (ACL) (solo servidores)

La negociación de la capa de seguridad es el proceso que utiliza COM para elegir la configuración de seguridad de un proxy cuando se crea. Este proceso implica comparar el marco de seguridad del servidor con la capa de seguridad del cliente y usar esos valores para crear una capa de seguridad predeterminada adecuada para el proxy. En los párrafos siguientes se explica dónde provienen los elementos de las mantas de seguridad del cliente y del servidor, y se describe cómo COM negocia la capa de seguridad para el proxy utilizando las operaciones de seguridad del cliente y del servidor.

El cliente y el servidor pueden llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para especificar sus respectivos mantas de seguridad. Si una aplicación no llama a **CoInitializeSecurity** explícitamente, com lo llama implícitamente para la aplicación, con los valores predeterminados adecuados. Para obtener más información sobre estos valores predeterminados, vea valores [predeterminados de seguridad com](com-security-defaults.md).

Algunos parámetros de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) se aplican cuando la aplicación es un servidor y otros se aplican cuando la aplicación es un cliente. Cuando la aplicación actúa como un servidor, estos parámetros son relevantes: una ACL, una lista de tuplas de servicio de autenticación/servicio de autorización/nombre de entidad de seguridad y un nivel de autenticación. La llamada de un servidor a **CoInitializeSecurity**, ya sea implícita o explícita, determina el marco de seguridad del servidor, que permanece fijo.

Cuando la aplicación actúa como cliente, los siguientes valores pasados a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) son relevantes: un nivel de autenticación, un nivel de suplantación, la identidad de autenticación y las capacidades. La llamada implícita o explícita de un cliente a **CoInitializeSecurity** indica el marco de seguridad que el cliente desea.

Cuando se crea un proxy, COM usa los valores especificados por la capa de seguridad del servidor y la capa de seguridad del cliente para negociar una manta de seguridad predeterminada que sea adecuada para el proxy. COM elige un servicio de autenticación que funciona tanto en el cliente como en el servidor. El servicio de autorización y el nombre de la entidad de seguridad se eligen para trabajar con el servicio de autenticación. Para el nivel de autenticación, COM elige el mayor de los niveles de autenticación especificados por el cliente y el servidor. El nivel de suplantación y las capacidades elegidas por COM son las especificadas por el cliente. La identidad de autenticación es la especificada por el cliente para el servicio de autenticación elegido.

Una vez que se ha calculado la capa de seguridad predeterminada, sus valores se asignan al proxy recién creado. El cliente puede invalidar la configuración de seguridad para el proxy mediante una llamada a [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Los valores especificados en **SetBlanket** no se negocian; simplemente se asignan al proxy especificado. Sin embargo, si los parámetros predeterminados (como \_ valor predeterminado de nivel de Imp de RPC C \_ \_ \_ ) se pasan a **SetBlanket**, com usa el algoritmo de negociación de la capa de seguridad que se ha descrito anteriormente para calcular los parámetros predeterminados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 