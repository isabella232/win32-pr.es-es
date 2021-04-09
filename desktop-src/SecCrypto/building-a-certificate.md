---
description: Explica las llamadas necesarias para compilar un certificado.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Creación de un certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913417"
---
# <a name="building-a-certificate"></a>Creación de un certificado

El orden de las llamadas en la creación de un certificado es el siguiente:

1.  La [*entidad de certificación*](../secgloss/c-gly.md) (CA) inicializa los módulos a través de llamadas a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) y [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (se produce una vez en la inicialización del servidor). La CA inicializará los módulos de directivas y de salida mediante una llamada a [**ICertPolicy2:: Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) y [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  El intermediario llama a la CA a través de [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (se produce una vez por inicialización intermediaria). El intermediario encuentra la cadena de configuración necesaria mediante una llamada a [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  El cliente llama al intermediario a través de una interfaz específica del intermediario (se produce una vez por solicitud). El cliente envía una [*solicitud de certificado*](../secgloss/c-gly.md) al intermediario. Esto puede ser, por ejemplo, que Microsoft Internet Explorer envíe una solicitud a través del [control de inscripción de certificados](certificate-enrollment-control.md) a Microsoft Internet Information Services.
4.  Intermediario a CA a través de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (se produce una vez por solicitud). El intermediario envía la solicitud de certificado a la CA a través de [**ICertRequest:: submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit). En el caso de Internet Information Services, esto puede realizarse a través de scripts de Active Server páginas.
5.  La CA llama al módulo de directivas a través de la interfaz [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (se produce una vez por solicitud). La entidad de certificación notifica al módulo de directivas que ha llegado una solicitud llamando a [**ICertPolicy:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest). El módulo de directivas puede examinar la solicitud y cambiar el certificado llamando a los métodos de la interfaz [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Después, el módulo de directivas puede indicar que la solicitud es correcta (si es así, el certificado se compila en este momento), se denegará la solicitud o se suspenderá la solicitud.
6.  Opta El administrador llama a la CA a través de la interfaz [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) . Si se suspende la solicitud, el administrador puede volver a enviar o denegar la solicitud, o modificar los atributos y las extensiones de la solicitud. Tenga en cuenta que si se vuelve a enviar la solicitud, el módulo de directivas tendrá otra oportunidad para procesar la solicitud (como resultado de una llamada a [**ICertPolicy:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). La tarea de reenviar o denegar la solicitud puede realizarse por medio del complemento MMC de la entidad de certificación u otra aplicación que use **ICertAdmin**.
7.  La CA llama al módulo de salida a través de la interfaz [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) . Si el módulo de salida ha indicado (cuando se llamó a [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) , en el paso 1) que está interesado en ver los certificados emitidos o las solicitudes que se mantienen pendientes, la CA llamará a [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  El módulo de salida llama a la CA a través de la interfaz [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) . El módulo de salida puede examinar la solicitud y el nuevo certificado llamando a los métodos de **ICertServerExit**.

 

 
