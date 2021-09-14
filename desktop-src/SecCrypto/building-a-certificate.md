---
description: Explica las llamadas necesarias para compilar un certificado.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Creación de un certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374910"
---
# <a name="building-a-certificate"></a>Creación de un certificado

El orden de las llamadas para crear un certificado es el siguiente:

1.  [*La entidad de*](../secgloss/c-gly.md) certificación (CA) inicializa los módulos a través de llamadas a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (se produce una vez en la inicialización del servidor). La CA inicializará la directiva y los módulos de salida llamando a [**ICertPolicy2::Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) e [**ICertExit::Initialize.**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize)
2.  El intermediario llama a la ca a través [**de ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (se produce una vez por inicialización intermediaria). El intermediario busca la cadena de configuración necesaria llamando a [**ICertConfig::GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  El cliente llama al intermediario a través de una interfaz específica del intermediario (se produce una vez por solicitud). El cliente envía una [*solicitud de certificado*](../secgloss/c-gly.md) al intermediario. Esto puede ser, por ejemplo, que Microsoft Internet Explorer una solicitud a través del [Control de inscripción](certificate-enrollment-control.md) de certificados para Microsoft Internet Information Services.
4.  Intermediario a ca a través de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (se produce una vez por solicitud). El intermediario envía la solicitud de certificado a la ca a través [**de ICertRequest::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit). En el caso de Internet Information Services, esto se podría hacer a través de scripts Active Server Pages.
5.  La CA llama al módulo de directivas a través de [**la interfaz ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (se produce una vez por solicitud). La ca notifica al módulo de directivas que ha llegado una solicitud llamando a [**ICertPolicy::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest). El módulo de directivas puede examinar la solicitud y cambiar el certificado llamando a métodos de la [**interfaz ICertServerPolicy.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) A continuación, el módulo de directivas puede indicar que la solicitud es correcta (si es así, el certificado se ha creado en este momento), la solicitud se va a denegar o se debe suspender la solicitud.
6.  (Opcional) El administrador llama a la ca a través de [**la interfaz ICertAdmin.**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) Si la solicitud se suspende, el administrador puede volver a enviarla o denegarla, o modificar los atributos y extensiones de la solicitud. Tenga en cuenta que si se vuelve a enviar la solicitud, el módulo de directivas tendrá otra oportunidad para procesar la solicitud (como resultado de una llamada a [**ICertPolicy::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). La tarea de volver a enviar o denegar la solicitud se puede realizar mediante el complemento MMC de la entidad de certificación u otra aplicación que use **ICertAdmin**.
7.  La CA llama al módulo exit a través de [**la interfaz ICertExit.**](/windows/desktop/api/Certexit/nn-certexit-icertexit) Si el módulo de salida ha indicado (cuando se llamó a [**ICertExit::Initialize,**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) en el paso 1) que está interesado en ver los certificados emitidos o las solicitudes pendientes, la CA llamará a [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  El módulo exit llama a la CA a través de [**la interfaz ICertServerExit.**](/windows/desktop/api/Certif/nn-certif-icertserverexit) El módulo exit puede examinar la solicitud y el nuevo certificado mediante una llamada a los métodos **de ICertServerExit**.

 

 
