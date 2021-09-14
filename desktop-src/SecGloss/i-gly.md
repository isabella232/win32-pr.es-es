---
description: Contiene definiciones de términos de seguridad que comienzan por la letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361822"
---
# <a name="i-security-glossary"></a>I (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [I](h-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](m-gly.md) [O](n-gly.md) [](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**
</dt> <dd>

Servicios de software que admiten la creación, configuración y administración de sitios web, junto con otras funciones de Internet. Internet Information Services protocolo de transferencia de noticias de red (NNTP), protocolo de transferencia de archivos (FTP) y protocolo simple de transferencia de correo (SMTP). IIS incorpora varias funciones de seguridad, permite aplicaciones CGI y proporciona servidores Gopher y FTP.

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**Suplantación**
</dt> <dd>

Mecanismo que permite que un proceso de servidor se ejecute mediante las credenciales de seguridad del cliente o de algún otro usuario que use las credenciales. Cuando el servidor suplanta al cliente, las operaciones realizadas por el servidor se realizan mediante las credenciales del cliente (suplantando las del usuario). La suplantación no permite que el servidor acceda a recursos remotos en nombre del cliente. Esto requiere delegación.

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**token de suplantación**
</dt> <dd>

Token de acceso que se ha creado para capturar la información de seguridad de un proceso de cliente, lo que permite a un servidor "suplantar" el proceso de cliente en operaciones de seguridad.

Consulte también token [*de acceso y*](a-gly.md) token [*principal.*](p-gly.md)

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**vector de inicialización**
</dt> <dd>

(IV) Secuencia de bytes aleatorios anexados al frente del texto no cifrado antes del cifrado por un cifrado de bloques. Agregar el vector de inicialización al principio del texto no cifrado elimina la posibilidad de que el bloque de texto cifrado inicial sea el mismo para dos mensajes cualquiera. Por ejemplo, si los mensajes siempre comienzan con un encabezado común (un encabezado de letra o una línea "From"), su texto cifrado inicial siempre sería el mismo, suponiendo que se usaran el mismo algoritmo criptográfico y clave simétrica. La adición de un vector de inicialización aleatorio evita que esto suceda.

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**datos internos**
</dt> <dd>

Los datos codificados que se usan como mensaje para otro mensaje codificado. Por ejemplo, un mensaje con sobre y su valor hash pueden ser los datos internos de un segundo mensaje.

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**contenido interno**
</dt> <dd>

Datos mejorados, como con una firma digital. Este término se usa principalmente al analizar los datos mejorados en un mensaje PKCS \# 7.

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**Integridad**
</dt> <dd>

La integridad y precisión de un mensaje después de que se haya enviado o almacenado.

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID de integridad**
</dt> <dd>

Identificador [*de seguridad*](s-gly.md) (SID) que representa un nivel de integridad. Un SID de integridad en la lista de [*control*](s-gly.md) de acceso del sistema (SACL) del descriptor de seguridad de un objeto especifica el nivel de integridad del objeto. Los SID de integridad de un token de acceso especifican el nivel de integridad del token.

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**
</dt> <dd>

Un nivel de solicitud de interrupción (IRQL) define la prioridad de hardware en la que funciona un procesador en un momento dado. En el Windows Driver Model, se puede interrumpir un subproceso que se ejecuta en un IRQL bajo para ejecutar código en un IRQL superior.

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**
</dt> <dd>

Vea vector *de inicialización*.

</dd> </dl>

 

 



