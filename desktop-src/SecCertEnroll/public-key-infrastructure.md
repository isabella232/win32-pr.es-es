---
description: La criptografía de clave pública (también denominada criptografía de clave asimétrica) usa un par de claves para cifrar y descifrar el contenido.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Infraestructura de clave pública
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a306f227a3e39c32b7e0eef2dbf1dc4ae9d59942096fb71428339d8a166a04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101135"
---
# <a name="public-key-infrastructure"></a>Infraestructura de clave pública

La criptografía de clave pública (también denominada criptografía de clave asimétrica) usa un par de claves para cifrar y descifrar el contenido. El par de claves consta de una clave pública y una privada que están relacionadas matemáticamente. Un individuo que pretende comunicarse de forma segura con otros usuarios puede distribuir la [*clave pública,*](/windows/desktop/SecGloss/p-gly) pero debe mantener el [*secreto de clave*](/windows/desktop/SecGloss/p-gly) privada. El contenido cifrado mediante una de las claves se puede descifrar mediante el otro. Supongamos, por ejemplo, que Bob quiere enviar un mensaje de correo electrónico seguro a Alice. Esto se puede lograr de la siguiente manera:

1.  Bob y Alice tienen sus propios pares de claves. Han mantenido sus claves privadas de forma segura y se han enviado sus claves públicas directamente entre sí.
2.  Bob usa la clave pública de Alice para cifrar el mensaje y lo envía a ella.
3.  Alice usa su clave privada para descifrar el mensaje.

En este ejemplo simplificado se resalta al menos una preocupación obvia que Bob debe tener sobre la clave pública que usó para cifrar el mensaje. Es decir, no puede saber con certeza que la clave que usó para el cifrado realmente pertenecía a Alice. Es posible que otra parte que supervisa el canal de comunicación entre Bob y Alice sustituyó una clave diferente.

El concepto de infraestructura de clave pública ha evolucionado para ayudar a solucionar este problema y otros. Una infraestructura de clave pública (PKI) consta de elementos de software y hardware que un tercero de confianza puede usar para establecer la integridad y la propiedad de una clave pública. La entidad de [](/windows/desktop/SecGloss/c-gly) confianza, denominada entidad de certificación (CA), normalmente lo consigue mediante la emisión de certificados binarios firmados (cifrados) que confirman la identidad del sujeto del certificado y enlazan esa identidad a la clave pública contenida en el certificado. La entidad de certificación firma el certificado mediante su clave privada. Emite la clave pública correspondiente a todas las partes interesadas en un certificado de entidad de certificación autofirmado. Cuando se usa una entidad de certificación, el ejemplo anterior se puede modificar de la siguiente manera:

1.  Suponga que la ca ha emitido un certificado digital firmado que contiene su clave pública. La entidad de certificación firma este certificado mediante la clave privada que corresponde a la clave pública del certificado.
2.  Alice y Bob aceptan usar la entidad de certificación para comprobar sus identidades.
3.  Alice solicita un certificado de clave pública de la entidad de certificación.
4.  La entidad de certificación comprueba su identidad, calcula un hash del contenido que formará su certificado, firma el hash mediante la clave privada que corresponde a la clave pública en el certificado de ca publicado, crea un nuevo certificado concatenando el contenido del certificado y el hash firmado y hace que el nuevo certificado esté disponible públicamente.
5.  Bob recupera el certificado, descifra el hash firmado mediante la clave pública de la entidad de certificación, calcula un nuevo hash del contenido del certificado y compara los dos hashes. Si los hash coinciden, se comprueba la firma y Bob puede suponer que la clave pública del certificado pertenece realmente a Alice.
6.  Bob usa la clave pública comprobada de Alice para cifrarle un mensaje.
7.  Alice usa su clave privada para descifrar el mensaje de Bob.

En resumen, el proceso de firma de certificado permite a Bob comprobar que la clave pública no se ha alterado o dañado durante el tránsito. Antes de emitir un certificado, la CA aplica un algoritmo hash al contenido, firma (cifra) el hash mediante su propia clave privada e incluye el hash cifrado en el certificado emitido. Bob comprueba el contenido del certificado descifrando el hash con la clave pública de la entidad de certificación, realizando un hash independiente del contenido del certificado y comparando los dos hashes. Si coinciden, Bob puede estar razonablemente seguro de que el certificado y la clave pública que contiene no se han modificado.

Una PKI típica consta de los siguientes elementos.

| Elemento                            | Descripción                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entidad de certificación<br/> | Actúa como raíz de confianza en una infraestructura de clave pública y proporciona servicios que autentican la identidad de personas, equipos y otras entidades de una red.<br/>      |
| Entidad de registro<br/>  | Está certificada por una CA raíz para emitir certificados para usos específicos permitidos por la raíz. En una PKI de Microsoft, una entidad de registro (RA) normalmente se denomina CA subordinada.<br/> |
| Base de datos de certificados<br/>    | Guarda las solicitudes de certificado y los certificados emitidos y revocados y las solicitudes de certificado en la CA o RA.<br/>                                                                       |
| Almacén de certificados<br/>       | Guarda los certificados emitidos y las solicitudes de certificado pendientes o rechazadas en el equipo local.<br/>                                                                                  |
| Servidor de archivado de claves<br/>     | Guarda las claves privadas cifradas en la base de datos de certificados para su recuperación después de la pérdida.<br/>                                                                                              |



 

La API de inscripción de certificados permite enviar solicitudes de archivo de certificados y claves a las entidades de certificación y registro e instalar el certificado emitido en un equipo local. No permite manipular directamente la base de datos de certificados o el almacén de certificados.

En los temas siguientes se describe la infraestructura de clave pública de Microsoft con más detalle:

-   [Certificados de clave pública X.509](about-x-509-public-key-certificates.md)
-   [Elementos PKI](about-pki-components.md)
-   [Modelos de confianza](about-trust-models.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

