---
description: La criptografía de clave pública (también denominada criptografía de clave asimétrica) usa un par de claves para cifrar y descifrar contenido.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Infraestructura de clave pública
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e4ff0b2b3912bc44851be105c2e2b15200eb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667721"
---
# <a name="public-key-infrastructure"></a>Infraestructura de clave pública

La criptografía de clave pública (también denominada criptografía de clave asimétrica) usa un par de claves para cifrar y descifrar contenido. El par de claves se compone de una clave pública y una privada que están relacionadas matemáticamente. Una persona que pretenda comunicarse de forma segura con otros usuarios puede distribuir la [*clave pública*](/windows/desktop/SecGloss/p-gly) , pero debe mantener el secreto de la [*clave privada*](/windows/desktop/SecGloss/p-gly) . El contenido cifrado mediante una de las claves se puede descifrar con el otro. Supongamos, por ejemplo, que Bob desea enviar un mensaje de correo electrónico seguro a Alice. Esto se puede lograr de la siguiente manera:

1.  Tanto Bob como Alice tienen sus propios pares de claves. Han mantenido sus claves privadas de forma segura y han enviado sus claves públicas directamente entre sí.
2.  Bob utiliza la clave pública de Alice para cifrar el mensaje y lo envía a ella.
3.  Alice usa su clave privada para descifrar el mensaje.

En este ejemplo simplificado se resalta al menos un problema obvio que Bob debe tener acerca de la clave pública que usó para cifrar el mensaje. Es decir, no puede saber con certeza que la clave que usó para el cifrado pertenecía realmente a Alice. Es posible que otra parte que supervisa el canal de comunicación entre Bob y Alice sustituya una clave diferente.

El concepto de infraestructura de clave pública ha evolucionado para ayudar a abordar este problema y otros. Una infraestructura de clave pública (PKI) consta de elementos de software y hardware que un tercero de confianza puede usar para establecer la integridad y la propiedad de una clave pública. La entidad de confianza, denominada [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA), lo consigue normalmente mediante la emisión de certificados binarios (cifrados) firmados que afirman la identidad del sujeto del certificado y enlazan esa identidad con la clave pública incluida en el certificado. La CA firma el certificado con su clave privada. Emite la clave pública correspondiente a todas las partes interesadas en un certificado de entidad de certificación autofirmado. Cuando se usa una CA, el ejemplo anterior se puede modificar de la siguiente manera:

1.  Supongamos que la entidad de certificación ha emitido un certificado digital firmado que contiene su clave pública. La CA firma automáticamente este certificado con la clave privada que corresponde a la clave pública del certificado.
2.  Alice y Bob acuerdan usar la CA para comprobar sus identidades.
3.  Alice solicita un certificado de clave pública de la CA.
4.  La entidad de certificación comprueba su identidad, calcula un hash del contenido que va a componer su certificado, firma el hash mediante la clave privada que corresponde a la clave pública del certificado de CA publicado, crea un nuevo certificado mediante la concatenación del contenido del certificado y el hash firmado y hace que el nuevo certificado esté disponible públicamente.
5.  Bob recupera el certificado, descifra el hash firmado mediante la clave pública de la CA, calcula un nuevo hash del contenido del certificado y compara los dos valores hash. Si los valores hash coinciden, se comprueba la firma y Bob puede suponer que la clave pública del certificado pertenece realmente a Alice.
6.  Bob usa la clave pública comprobada de Alice para cifrar un mensaje.
7.  Alice usa su clave privada para descifrar el mensaje de Bob.

En Resumen, el proceso de firma de certificados permite a Bob comprobar que la clave pública no se ha manipulado o dañado durante el tránsito. Antes de emitir un certificado, la entidad de certificación aplica un algoritmo hash al contenido, firma (cifra) el hash mediante su propia clave privada e incluye el hash cifrado en el certificado emitido. Bob comprueba el contenido del certificado mediante el descifrado del hash con la clave pública de la CA, la realización de un hash independiente del contenido del certificado y la comparación de los dos valores hash. Si coinciden, Bob puede estar razonablemente seguro de que el certificado y la clave pública que contiene no se han modificado.

Una PKI típica consta de los siguientes elementos.

| Elemento                            | Descripción                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entidad de certificación<br/> | Actúa como la raíz de confianza en una infraestructura de clave pública y proporciona servicios que autentican la identidad de individuos, equipos y otras entidades de una red.<br/>      |
| Autoridad de registro<br/>  | Está certificado por una entidad de certificación raíz para emitir certificados para usos específicos permitidos por la raíz. En una PKI de Microsoft, una autoridad de registro (RA) se denomina normalmente entidad de certificación subordinada.<br/> |
| Base de datos de certificados<br/>    | Guarda las solicitudes de certificados y los certificados emitidos y revocados y las solicitudes de certificado en la entidad de certificación o RA.<br/>                                                                       |
| Almacén de certificados<br/>       | Guarda los certificados emitidos y las solicitudes de certificados pendientes o rechazadas en el equipo local.<br/>                                                                                  |
| Servidor de archivo de claves<br/>     | Guarda las claves privadas cifradas en la base de datos de certificados para su recuperación después de la pérdida.<br/>                                                                                              |



 

La API de inscripción de certificados permite enviar solicitudes de archivo de certificado y clave a las entidades de certificación y de registro, e instalar el certificado emitido en un equipo local. No permite manipular directamente la base de datos de certificados o el almacén de certificados.

En los temas siguientes se describe la infraestructura de clave pública de Microsoft con más detalle:

-   [Certificados de clave pública X. 509](about-x-509-public-key-certificates.md)
-   [Elementos PKI](about-pki-components.md)
-   [Modelos de confianza](about-trust-models.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

