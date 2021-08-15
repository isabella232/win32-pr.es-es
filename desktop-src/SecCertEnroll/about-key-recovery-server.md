---
description: Se puede configurar una entidad de certificación (CA) de Microsoft para archivar y recuperar la clave privada asociada a la clave pública enviada en la solicitud de certificado.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Servidor de recuperación de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a313ac46bf540d6d0f356f7e2c4910e31bee1f2a4268931ac6a942085505b423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903778"
---
# <a name="key-recovery-server"></a>Servidor de recuperación de claves

Se puede configurar una entidad de certificación (CA) de Microsoft para archivar y recuperar la clave privada asociada a la clave pública enviada en la solicitud de certificado. La recuperación es útil si se pierde una clave. De forma predeterminada, solo se pueden archivar las claves de cifrado. No es necesario archivar las claves diseñadas solo para firmar porque solo se necesita la clave pública para comprobar una firma si se pierde la clave de firma privada.

Para archivar una clave, la CA debe configurarse para emitir certificados del agente de recuperación de claves (SSM) y para que ya haya emitido al menos uno. Un agente de recuperación de claves es un administrador autorizado por una organización para descifrar claves privadas. Para mejorar la seguridad, se recomienda asignar el agente de recuperación de claves y los roles de administrador de certificados a distintos usuarios, que el administrador de certificados pueda recuperar pero no descifrar las claves archivadas y que el agente de recuperación de claves pueda descifrar las claves pero no recuperarlas.

## <a name="key-archival"></a>Archivo de claves

Normalmente, un cliente solicita un certificado mediante una plantilla. Si la plantilla requiere que se archive la clave privada, el cliente y la entidad de certificación realizan los pasos siguientes:

1.  El cliente recupera y valida el certificado de intercambio de ca para determinar si se ha firmado con la misma clave que se usó para firmar el certificado de firma de ca. Esto garantiza que la única ENTIDAD de certificación que puede descifrar la clave privada es la entidad de certificación desde la que se solicita un certificado.
2.  La clave pública del certificado de intercambio de ca se usa para cifrar la clave privada asociada a la solicitud de certificado y la solicitud se envía a la ca.
3.  La CA usa la clave privada asociada a su certificado de intercambio para descifrar la clave privada enviada por el cliente y comprueba que las claves públicas y privadas de la solicitud están relacionadas.
4.  La entidad de certificación cifra la clave privada mediante la clave pública en el certificado DESO. Si la ca ha emitido varios certificados DEER, cifra la clave privada una vez con cada clave pública disponible para que cualquier agente de recuperación de claves autorizado pueda recuperar una clave. Las claves privadas cifradas se almacenan en la base de datos de certificados.
5.  La ca libera todas las referencias a la clave privada y libera y ceros de forma segura toda la memoria que contenía la clave. Esto garantiza que la entidad de certificación no tenga acceso adicional a la clave en formato de texto no cifrado.

> [!Note]  
> Solo se puede usar una solicitud de CMC para el archivo de claves. Las solicitudes de CMC se representan mediante la [**interfaz IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)

 

## <a name="key-recovery"></a>Recuperación de claves

La recuperación de claves no es compatible directamente con Servicios de certificados de Active Directory o la API de inscripción de certificados. Sin embargo, Microsoft proporciona las siguientes aplicaciones para ayudar con el proceso:

-   Certutil.exe es un programa de línea de comandos que se puede usar para recuperar información de configuración de ca, comprobar certificados, pares de claves y cadenas de certificados, y realizar copias de seguridad y restaurar claves. Se incluye en sistemas operativos de servidor a partir de Windows Server 2003.
-   Krecover.exe es un programa basado en cuadros de diálogo que permite la recuperación de claves. Se incluye con el Kit de recursos a partir de Windows Server 2003.

Los pasos siguientes se realizan para recuperar una clave privada:

1.  El administrador de certificados busca posibles candidatos para la recuperación de claves en la base de datos de certificados mediante el nombre del certificado, solicitante o usuario. El **comando Certutil** **-getkey** se puede usar para este propósito.
2.  Una vez que el administrador de certificados tiene una lista de certificados, se llama de nuevo al comando **-getkey** con un número de serie de certificado específico o una huella digital para recuperar un archivo PKCS 7 que contiene el certificado PKCS 7, la cadena de certificados de usuario y la clave privada que se ha cifrado durante el archivado mediante la clave pública \# PKCS 7.
3.  El administrador de certificados pasa el control del proceso al agente de recuperación de claves cuya clave privada coincide con la clave pública contenida en el certificado DE LAN.
4.  El agente de recuperación de claves descifra la clave privada archivada devuelta en el archivo PKCS \# 7 mediante la clave privada DEIA. Para ello, use el comando **Certutil** **-recoverkey,** que coloca la clave en un archivo PKCS 12 protegido con \# contraseña. Al cliente se le debe proporcionar la contraseña a través de un mecanismo seguro fuera de banda.
5.  El cliente importa el archivo PKCS \# 12 y usa la contraseña para recuperar la clave.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 



