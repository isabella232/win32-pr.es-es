---
title: Negociación de negociación de negociación de seguridad
description: Negociación de negociación de negociación de seguridad
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369632"
---
# <a name="security-blanket-negotiation"></a>Negociación de negociación de negociación de seguridad

Una medida de seguridad es un grupo de valores que describen la configuración de seguridad que se aplica a todos los servidores proxy de un proceso o solo a un proxy de interfaz determinado. Una zona de seguridad consta de los siguientes valores:

-   Servicio de autenticación
-   Servicio de autorización
-   Nombre principal
-   Nivel de autenticación
-   Nivel de suplantación
-   Identidad de autenticación
-   Capacidades
-   Una lista de control de acceso (ACL) (solo servidores)

La negociación de negociación de negociación de negociación de seguridad es el proceso que COM usa para elegir la configuración de seguridad de un proxy cuando se crea. Este proceso implica comparar la seguridad del servidor con la seguridad del cliente y usar esos valores para crear una medida de seguridad predeterminada adecuada para el proxy. En los párrafos siguientes se explica de dónde proceden las garantías de seguridad del cliente y del servidor, y se describe cómo COM negocia la seguridad del proxy mediante las medidas de seguridad del cliente y del servidor.

El cliente y el servidor pueden llamar a [**CoInitializeSecurity para**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) especificar sus respectivos valores de seguridad. Si una aplicación no llama explícitamente a **CoInitializeSecurity,** COM la llama implícitamente para la aplicación, con los valores predeterminados adecuados. Para obtener más información sobre estos valores predeterminados, vea [Valores predeterminados de seguridad COM.](com-security-defaults.md)

Algunos parámetros de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) se aplican cuando la aplicación es un servidor y otros cuando la aplicación es un cliente. Cuando la aplicación actúa como servidor, estos parámetros son relevantes: una ACL, una lista de tuplas de servicio de autenticación, servicio de autorización o nombre principal y un nivel de autenticación. La llamada de un servidor a **CoInitializeSecurity**, ya sea implícita o explícita, determina la matriz de seguridad del servidor, que permanece fija.

Cuando la aplicación actúa como cliente, los siguientes valores pasados a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) son relevantes: un nivel de autenticación, un nivel de suplantación, la identidad de autenticación y las funcionalidades. La llamada implícita o explícita de un cliente a **CoInitializeSecurity** indica la seguridad que quiere el cliente.

Cuando se crea un proxy, COM usa los valores especificados por la negociación de seguridad del servidor y la negociación de seguridad del cliente para negociar una negociación de seguridad predeterminada que sea adecuada para el proxy. COM elige un servicio de autenticación que funciona tanto en el cliente como en el servidor. El servicio de autorización y el nombre principal se eligen para trabajar con el servicio de autenticación. Para el nivel de autenticación, COM elige el superior de los niveles de autenticación especificados por el cliente y el servidor. El nivel de suplantación y las funcionalidades elegidas por COM son los especificados por el cliente. La identidad de autenticación es la especificada por el cliente para el servicio de autenticación elegido.

Una vez que se ha calculado el límite de seguridad predeterminado, sus valores se asignan al proxy recién creado. El cliente puede invalidar la configuración de seguridad del proxy llamando a [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Los valores especificados en **SetBlanket** no se negocian; simplemente se asignan al proxy especificado. Sin embargo, si los parámetros predeterminados (como RPC C IMP LEVEL DEFAULT) se pasan a \_ \_ \_ \_ **SetBlanket,** COM usa el algoritmo de negociación de seguridad descrito anteriormente para calcular los parámetros predeterminados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 