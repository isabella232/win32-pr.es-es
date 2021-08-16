---
description: Client-Side requisitos de suplantación
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side requisitos de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb47c2ffb5f3b8e443d2dc50add83a39b5dfc1ee31a6909c34b0170a85db11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308534"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side requisitos de suplantación

Se pueden especificar las dos opciones siguientes en relación con la suplantación en el lado cliente:

-   Nivel de suplantación, que indica la disposición del cliente para que el servidor use su identidad.
-   Una configuración del servicio Active Directory a través del cual la cuenta de cliente se puede marcar como "La cuenta es confidencial y no se puede delegar", lo que deshabilitará la delegación.

El nivel de suplantación se puede establecer de varias maneras. Si el cliente no indica un nivel de suplantación, COM usará el valor predeterminado de todo el equipo. El valor predeterminado de todo el equipo se puede establecer mediante la herramienta administrativa Servicios de componentes o Dcomcnfg.exe. El cliente también puede indicar un nivel de suplantación preferido administrativamente con Dcomcnfg.exe.

El cliente puede indicar el nivel de suplantación mediante programación, mediante [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)(equivalente a [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), al que se puede llamar con tanta frecuencia como sea necesario) o [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), al que se puede llamar una vez por proceso.

Si el cliente indica la suplantación de nivel de delegado (la autoridad más amplia que puede conceder al servidor), el cliente debe ejecutarse con una identidad que esté configurada correctamente en el servicio Active Directory para permitir que se delegue su identidad.

Para obtener más detalles sobre los niveles de suplantación y los requisitos para que la delegación funcione, vea [Delegación y suplantación.](/windows/desktop/com/delegation-and-impersonation)

Las aplicaciones COM+ siempre pueden actuar como clientes, por supuesto. Cuando la aplicación COM+ realiza una llamada a otra aplicación o recurso, expresa un nivel de suplantación. Para las aplicaciones de servidor COM+, puede establecer un nivel de suplantación de forma administrativa. Las aplicaciones de biblioteca COM+ no pueden establecer su propio nivel de suplantación; usan en su lugar la del proceso de host. Para obtener información sobre cómo establecer la suplantación para una aplicación COM+, vea [Establecer un nivel de suplantación.](setting-an-impersonation-level.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Ocultación](cloaking.md)
</dt> <dt>

[Requisitos del lado servidor para la suplantación](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
