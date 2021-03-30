---
description: Contiene definiciones de términos de seguridad que comienzan por la letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082990"
---
# <a name="i-security-glossary"></a>I (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**
</dt> <dd>

Servicios de software que admiten la creación, configuración y administración de sitios web, junto con otras funciones de Internet. Internet Information Services incluyen el protocolo de transferencia de noticias en red (NNTP), el protocolo de transferencia de archivos (FTP) y el Protocolo simple de transferencia de correo (SMTP). IIS incorpora varias funciones de seguridad, permite aplicaciones CGI y proporciona servidores Gopher y FTP.

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**suplantación**
</dt> <dd>

Mecanismo que permite a un proceso de servidor ejecutarse mediante las credenciales de seguridad del cliente o algún otro usuario que use las credenciales. Cuando el servidor suplanta al cliente, las operaciones realizadas por el servidor se realizan mediante las credenciales del cliente (suplantando al usuario). La suplantación no permite que el servidor tenga acceso a los recursos remotos en nombre del cliente. Esto requiere delegación.

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**token de suplantación**
</dt> <dd>

Un token de acceso que se ha creado para capturar la información de seguridad de un proceso de cliente, lo que permite a un servidor "suplantar" el proceso de cliente en operaciones de seguridad.

Vea también [*token de acceso*](a-gly.md) y [*token principal*](p-gly.md).

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**Vector de inicialización**
</dt> <dd>

(IV) una secuencia de bytes aleatorios anexados al anverso del texto sin formato antes del cifrado mediante un cifrado de bloque. Al agregar el vector de inicialización al principio del texto simple, se elimina la posibilidad de tener el bloque de texto cifrado inicial igual para dos mensajes cualesquiera. Por ejemplo, si los mensajes siempre comienzan con un encabezado común (un membrete o una línea "de"), su texto cifrado inicial siempre será el mismo, suponiendo que se usó el mismo algoritmo criptográfico y clave simétrica. La adición de un vector de inicialización aleatorio evita que esto suceda.

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**datos internos**
</dt> <dd>

Cualquier dato codificado que se use como mensaje para otro mensaje codificado. Por ejemplo, un mensaje con doble cifrado y su valor hash pueden ser los datos internos de un segundo mensaje.

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**contenido interno**
</dt> <dd>

Datos que se han mejorado, como con una firma digital. Este término se usa principalmente cuando se analizan datos mejorados en un \# mensaje PKCS 7.

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integración**
</dt> <dd>

La integridad y la precisión de un mensaje después de que se haya enviado o almacenado.

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID de integridad**
</dt> <dd>

Un [*identificador de seguridad*](s-gly.md) (SID) que representa un nivel de integridad. Un SID de integridad en la [*lista de control de acceso de sistema*](s-gly.md) (SACL) del descriptor de seguridad de un objeto especifica el nivel de integridad del objeto. Los SID de integridad de un token de acceso especifican el nivel de integridad del token.

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**
</dt> <dd>

Un nivel de solicitud de interrupción (IRQL) define la prioridad de hardware en la que un procesador funciona en un momento dado. En el Modelo de controlador de Windows, se puede interrumpir un subproceso que se ejecuta en un IRQL bajo para ejecutar código en una IRQL superior.

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**CUARTA**
</dt> <dd>

Consulte *Vector de inicialización*.

</dd> </dl>

 

 



