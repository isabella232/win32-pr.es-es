---
description: Se puede configurar una entidad de certificación (CA) de Microsoft para archivar y recuperar la clave privada asociada a la clave pública enviada en la solicitud de certificado.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Servidor de recuperación de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9fd60b7ee6596b98953d382978be64695c035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909646"
---
# <a name="key-recovery-server"></a>Servidor de recuperación de claves

Se puede configurar una entidad de certificación (CA) de Microsoft para archivar y recuperar la clave privada asociada a la clave pública enviada en la solicitud de certificado. La recuperación resulta útil si se pierde una clave. De forma predeterminada, solo se pueden archivar las claves de cifrado. No es necesario archivar las claves destinadas únicamente a la firma, ya que solo se necesita la clave pública para comprobar una firma si se pierde la clave de firma privada.

Para archivar una clave, la CA debe estar configurada para emitir certificados del agente de recuperación de claves (KRA) y para que ya haya emitido al menos uno. Un agente de recuperación de claves es un administrador autorizado por una organización para descifrar las claves privadas. Para mejorar la seguridad, se recomienda que el agente de recuperación de claves y los roles de administrador de certificados se asignen a diferentes usuarios, que el administrador de certificados pueda recuperar pero no descifrar las claves archivadas y que el agente de recuperación de claves pueda descifrar las claves pero no recuperarlas.

## <a name="key-archival"></a>Archivo de claves

Un cliente normalmente solicita un certificado mediante una plantilla. Si la plantilla requiere que se Archive la clave privada, el cliente y la CA realizan los siguientes pasos:

1.  El cliente recupera y valida el certificado de intercambio de la entidad de certificación para determinar si se ha firmado con la misma clave que se usó para firmar el certificado de firma de la entidad de certificación. Esto garantiza que la única CA que puede descifrar la clave privada sea la CA desde la que se solicita un certificado.
2.  La clave pública del certificado de intercambio de CA se usa para cifrar la clave privada asociada a la solicitud de certificado y la solicitud se envía a la CA.
3.  La entidad de certificación usa la clave privada asociada con su certificado de Exchange para descifrar la clave privada enviada por el cliente y comprueba que las claves públicas y privadas de la solicitud estén relacionadas.
4.  La entidad de certificación cifra la clave privada mediante la clave pública del certificado de KRA. Si la CA ha emitido varios certificados de KRA, cifra la clave privada una vez con cada clave pública disponible para que cualquier agente de recuperación de claves autorizado pueda recuperar una clave. Las claves privadas cifradas se almacenan en la base de datos de certificados.
5.  La entidad de certificación libera todas las referencias a la clave privada y libera de forma segura y pone a cero toda la memoria que contenía la clave. Esto garantiza que la CA no tiene más acceso a la clave en formato de texto no cifrado.

> [!Note]  
> Solo se puede usar una solicitud CMC para el archivo de claves. Las solicitudes CMC se representan mediante la interfaz [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

 

## <a name="key-recovery"></a>Recuperación de claves

La recuperación de claves no es compatible directamente con los servicios de Certificate Server de Active Directory o la API de inscripción de certificados. Sin embargo, Microsoft no proporciona las siguientes aplicaciones para ayudar con el proceso:

-   Certutil.exe es un programa de línea de comandos que se puede usar para recuperar información de configuración de la entidad de certificación, comprobar certificados, pares de claves y cadenas de certificados, así como realizar copias de seguridad y restaurar claves. Se incluye en sistemas operativos de servidor a partir de Windows Server 2003.
-   Krecover.exe es un programa basado en cuadros de diálogo que permite la recuperación de claves. Se incluye con el kit de recursos a partir de Windows Server 2003.

Los pasos siguientes se realizan para recuperar una clave privada:

1.  El administrador de certificados localiza los posibles candidatos para la recuperación de claves en la base de datos de certificados mediante el nombre del certificado, el solicitante o el usuario. Para este fin, se puede usar el comando **certutil** **-getKey** .
2.  Una vez que el administrador de certificados tiene una lista de certificados, se llama de nuevo al comando **-getKey** con un número de serie de certificado específico o una impresión en miniatura para recuperar un \# archivo PKCS 7 que contiene el certificado de Kra, la cadena de certificados de usuario y la clave privada que se cifró durante el archivado mediante la clave pública de Kra.
3.  El administrador de certificados pasa el control del proceso al agente de recuperación de claves cuya clave privada coincide con la clave pública incluida en el certificado de KRA.
4.  El agente de recuperación de claves descifra la clave privada archivada devuelta en el \# archivo PKCS 7 mediante la clave privada de Kra. Esto puede realizarse mediante el comando **certutil** **-recoverkey** , que coloca la clave en un archivo PKCS 12 protegido con contraseña \# . El cliente debe tener la contraseña a través de un mecanismo seguro fuera de banda.
5.  El cliente importa el \# archivo PKCS 12 y usa la contraseña para recuperar la clave.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 



