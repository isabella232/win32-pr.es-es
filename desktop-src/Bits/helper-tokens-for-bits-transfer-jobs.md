---
title: Tokens auxiliares para trabajos de transferencia de BITS
description: Tokens auxiliares para trabajos de transferencia de BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a22708b11bd07165166f647454c05663d59f6cfeddde659a9bb5903d5a9606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528685"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Tokens auxiliares para trabajos de transferencia de BITS

En Windows Vista, el servicio Servicio de transferencia inteligente en segundo plano (BITS) permite a una aplicación asociar un único token de seguridad a un trabajo de transferencia de BITS. A continuación, el trabajo de transferencia de BITS usa este token para la autenticación y para el acceso a los recursos locales y remotos.

En Windows 7, el servicio BITS asocia un token adicional a un trabajo de transferencia de BITS. El trabajo de transferencia de BITS se puede configurar con un token de seguridad adicional, que es un token de suplantación creado por una aplicación que llama a la API COM de BITS. Este modelo de token auxiliar permite a las aplicaciones usar simultáneamente dos tokens de seguridad diferentes para acceder a archivos locales, certificados del lado cliente, archivos remotos y servidores proxy. Por ejemplo, se crea un trabajo de transferencia de BITS que escribe los datos descargados en un directorio local con privilegios y, a continuación, presenta una identidad de dominio con derechos bajos al servidor HTTP y al servidor proxy.

Una aplicación, normalmente un Windows, especifica un token auxiliar mediante la nueva interfaz [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions). El objeto de trabajo BITS implementa esta interfaz. La aplicación llama a [**IBackgroundCopyJob::QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) para obtener el puntero de interfaz. La aplicación suplanta la identidad del asistente y llama a [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para pasar el token al servicio BITS. A continuación, la aplicación especifica los recursos a los que se aplica el token pasando un conjunto de marcas de bits mediante [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). La aplicación borra todas las marcas (con **SetHelperTokenFlags** de nuevo) para revertir el comportamiento. El servicio BITS almacena las marcas de bits y el token en el trabajo de transferencia de BITS.

Cuando el propietario de los trabajos de transferencia de BITS cierra la sesión, el servicio BITS descarta los tokens auxiliares asociados al trabajo de transferencia. Si la transferencia no se completa, el servicio BITS coloca el trabajo en un estado de error con el código de error **BG \_ E TOKEN \_ \_ REQUIRED** y descarta el token auxiliar. La aplicación cliente puede actualizar el token llamando a [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) y, a continuación, puede reanudar el trabajo de transferencia de BITS. Como alternativa, la aplicación cliente puede borrar las marcas de token del asistente mediante [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) y, a continuación, reanudar el trabajo de transferencia sin un token auxiliar.

Del mismo modo, cuando el propietario de una sesión de terminal Services cierra sesión, el servicio BITS debe descartar los tokens auxiliares de esa sesión y colocar los trabajos de transferencia afectados en un estado de error con el código de error **BG \_ E TOKEN \_ \_ REQUIRED.**

El modelo de token auxiliar requiere un cambio en la directiva de control de acceso de BITS. Las versiones anteriores de BITS implementaban comprobaciones de acceso en cada llamada de método. A partir Windows 7, la comprobación de acceso debe realizarse dentro de la [**llamada IBackgroundCopyJob::QueryInterface;**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) de lo contrario, es posible que el token del asistente no tenga acceso al trabajo de transferencia.

> [!Note]  
> Las implementaciones anteriores requerían eficazmente que los usuarios de BITS tengan privilegios de administrador para establecer tokens auxiliares. A partir de Windows 10, versión 1607, los usuarios de BITS que no son administradores pueden usar [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para establecer tokens auxiliares que no son de administrador en los trabajos bits que poseen. Este cambio permite a los usuarios de BITS que no son administradores (como los servicios de descarga en segundo plano que se ejecutan en la [cuenta NetworkService)](/windows/desktop/Services/networkservice-account)establecer tokens auxiliares.
>
> En concreto, la implementación se ha cambiado para permitir que los usuarios sin privilegios de administrador establezcan tokens auxiliares, siempre y cuando se cumplen las condiciones siguientes:
>
> -   durante la [**llamada a IBackgroundCopyJob::QueryInterface,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) el SID del token del subproceso del autor de la llamada es el mismo que el SID de la cuenta de usuario del propietario del trabajo y
> -   Cuando se llama a [**IBitsTokenOptions::SetHelperToken,**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) el token auxiliar no tiene habilitado el SID de administrador (ADMINISTRADORES DE **\_ \_ RID \_** DE ALIAS DE DOMINIO).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 