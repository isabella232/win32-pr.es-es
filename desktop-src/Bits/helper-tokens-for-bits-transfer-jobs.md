---
title: Tokens de aplicación auxiliar para trabajos de transferencia de BITS
description: Tokens de aplicación auxiliar para trabajos de transferencia de BITS
ms.assetid: f29f9870-e406-472b-9342-203def7453ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52925a6e0d5a9601e21848d514214bfb843f6246
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488259"
---
# <a name="helper-tokens-for-bits-transfer-jobs"></a>Tokens de aplicación auxiliar para trabajos de transferencia de BITS

En Windows Vista, el servicio Servicio de transferencia inteligente en segundo plano (BITS) permite a una aplicación asociar un solo token de seguridad a un trabajo de transferencia de BITS. A continuación, el trabajo de transferencia de BITS usa este token para la autenticación y para el acceso a los recursos locales y remotos.

En Windows 7, el servicio BITS asocia un token adicional a un trabajo de transferencia de BITS. El trabajo de transferencia de BITS se puede configurar con un token de seguridad adicional, que es un token de suplantación creado por una aplicación que llama a la API de COM de BITS. Este modelo de token auxiliar permite a las aplicaciones usar simultáneamente dos tokens de seguridad diferentes para tener acceso a archivos locales, certificados del lado cliente, archivos remotos y servidores proxy. Por ejemplo, se crea un trabajo de transferencia de BITS que escribe los datos descargados en un directorio local con privilegios y, a continuación, presenta una identidad de dominio con derechos reducidos para el servidor proxy y el servidor HTTP.

Una aplicación, normalmente un servicio de Windows, especifica un token auxiliar mediante el uso de la nueva interfaz [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions). Esta interfaz se implementa mediante el objeto de trabajo de BITS. La aplicación llama a [**IBackgroundCopyJob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) para obtener el puntero de interfaz. La aplicación suplanta la identidad del ayudante y llama a [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para pasar el token al servicio bits. A continuación, la aplicación especifica los recursos a los que se aplica el token pasando un conjunto de marcadores de bits mediante [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags). La aplicación borra todas las marcas (usando de nuevo **SetHelperTokenFlags** ) para revertir el comportamiento. El servicio BITS almacena las marcas de bits y el token en el trabajo de transferencia de BITS.

Cuando el propietario de los trabajos de transferencia de BITS cierra la sesión, el servicio BITS descarta cualquier token auxiliar que esté asociado con el trabajo de transferencia. Si no se completa la transferencia, el servicio BITS coloca el trabajo en un estado de error con el código de error requerido por el **\_ \_ token \_ de BG e** y descarta el token de la aplicación auxiliar. La aplicación cliente puede actualizar el token llamando a [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) y, a continuación, puede reanudar el trabajo de transferencia de bits. Como alternativa, la aplicación cliente puede borrar las marcas de tokens auxiliares mediante [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) y, a continuación, reanudar el trabajo de transferencia sin un token auxiliar.

Del mismo modo, cuando el propietario de una sesión de Terminal Services cierra la sesión, el servicio BITS debe descartar los tokens auxiliares de esa sesión y colocar los trabajos de transferencia afectados en un estado de error con el código de error **\_ requerido del \_ token \_ de BG E** .

El modelo de token auxiliar requiere un cambio en la Directiva de control de acceso de BITS. Las versiones anteriores de BITS implementaban comprobaciones de acceso en cada llamada al método. A partir de Windows 7, la comprobación de acceso se debe realizar dentro de la llamada a [**IBackgroundCopyJob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) ; de lo contrario, el token auxiliar podría no tener acceso al trabajo de transferencia.

> [!Note]  
> Las implementaciones más antiguas requerían eficazmente que los usuarios de BITS dispongan de privilegios de administrador para establecer tokens auxiliares. A partir de Windows 10, versión 1607, los usuarios de BITS que no son administradores pueden usar [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para establecer tokens auxiliares que no son de administrador en trabajos de bits que poseen. Este cambio permite a los usuarios de BITS que no son administradores (como los servicios de descarga en segundo plano que se ejecutan con la [cuenta NetworkService](/windows/desktop/Services/networkservice-account)) establecer tokens auxiliares.
>
> En concreto, la implementación se ha cambiado para permitir que los usuarios sin privilegios de administrador establezcan tokens auxiliares, siempre y cuando se cumplan las condiciones siguientes:
>
> -   durante la llamada a [**IBackgroundCopyJob:: QueryInterface**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , el SID del token thread's del llamador es el mismo que el SID de la cuenta de usuario del propietario del trabajo.
> -   Cuando se llama a [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) , el token auxiliar no tiene habilitado el SID de administrador (**administradores de RID de alias de dominio \_ \_ \_**).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> </dl>

 

 