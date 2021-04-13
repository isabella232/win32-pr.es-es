---
description: Requisitos de Client-Side para la suplantación
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Requisitos de Client-Side para la suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360081"
---
# <a name="client-side-requirements-for-impersonation"></a>Requisitos de Client-Side para la suplantación

Se pueden especificar las dos configuraciones siguientes en relación con la suplantación en el lado cliente:

-   Nivel de suplantación, que indica que el cliente está dispuesto a hacer que el servidor use su identidad.
-   Una configuración en el servicio Active Directory a través de la cual la cuenta de cliente se puede marcar como "la cuenta es confidencial y no se puede delegar", lo que deshabilitará la delegación.

El nivel de suplantación se puede establecer de varias maneras. Si el cliente no indica un nivel de suplantación, COM utilizará el valor predeterminado para todo el equipo. El valor predeterminado para todo el equipo se puede establecer mediante la herramienta administrativa Servicios de componentes o Dcomcnfg.exe. El cliente también puede indicar un nivel de suplantación preferible administrativamente con Dcomcnfg.exe.

El cliente puede indicar el nivel de suplantación mediante programación, mediante [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)(equivalente a [**IClientSecurity:: SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), al que se puede llamar con tanta frecuencia como sea necesario) o a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), al que se puede llamar una vez por cada proceso.

Si el cliente indica la suplantación de nivel de delegado (la autoridad más amplia que puede conceder al servidor), el cliente debe ejecutarse con una identidad que esté configurada correctamente en el servicio de Active Directory para permitir la delegación de su identidad.

Para obtener más información sobre los niveles de suplantación y los requisitos de delegación, consulte [delegación y suplantación](/windows/desktop/com/delegation-and-impersonation).

Por supuesto, las aplicaciones COM+ siempre pueden actuar como clientes. Cuando la aplicación COM+ realiza una llamada a otra aplicación o recurso, expresa un nivel de suplantación. En el caso de las aplicaciones de servidor COM+, puede establecer un nivel de suplantación de forma administrativa. Las aplicaciones de biblioteca COM+ no pueden establecer su propio nivel de suplantación; en su lugar, usan el del proceso de host. Para obtener información sobre cómo establecer la suplantación para una aplicación COM+, vea [establecer un nivel de suplantación](setting-an-impersonation-level.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Esconder](cloaking.md)
</dt> <dt>

[Requisitos del servidor para la suplantación](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
