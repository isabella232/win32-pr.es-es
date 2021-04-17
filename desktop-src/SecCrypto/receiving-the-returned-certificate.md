---
description: Explica cómo una aplicación recibe un certificado.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Recibir el certificado devuelto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688423"
---
# <a name="receiving-the-returned-certificate"></a><span data-ttu-id="d6ad4-103">Recibir el certificado devuelto</span><span class="sxs-lookup"><span data-stu-id="d6ad4-103">Receiving the Returned Certificate</span></span>

<span data-ttu-id="d6ad4-104">Cuando la entidad de certificación (CA) ha comprobado la información de identidad del solicitante y se ha asegurado de que el solicitante es el propietario de la clave privada y de que los datos sobre el solicitante son precisos, la entidad de certificación crea un certificado X. 509, lo firma, lo empaqueta con los demás certificados necesarios (como el propio certificado de la entidad de certificación) en un mensaje y envía el mensaje al solicitante.</span><span class="sxs-lookup"><span data-stu-id="d6ad4-104">When the certification authority (CA) has verified the requester's identity information and is satisfied that the requester is the owner of the private key and that the data about that requester is accurate, the CA constructs an X.509 certificate, signs it, packages it with any other needed certificates (such as the CA's own certificate) in a message, and sends the message to the requester.</span></span> <span data-ttu-id="d6ad4-105">El mensaje puede ser un \# mensaje PKCS 7 o una respuesta CMC (las plantillas V2 dan como resultado una respuesta CMC).</span><span class="sxs-lookup"><span data-stu-id="d6ad4-105">The message can be a PKCS \#7 message or a CMC response (V2 templates result in a CMC response).</span></span>

<span data-ttu-id="d6ad4-106">La aplicación receptora pasa el mensaje al control de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="d6ad4-106">The receiving application passes the message to the Certificate Enrollment Control.</span></span> <span data-ttu-id="d6ad4-107">Después, el control de inscripción de certificados abre el mensaje y extrae los certificados.</span><span class="sxs-lookup"><span data-stu-id="d6ad4-107">The Certificate Enrollment Control then opens the message and extracts the certificates.</span></span> <span data-ttu-id="d6ad4-108">Se muestra al usuario un cuadro de diálogo en el que se le pregunta si el usuario aceptará certificados autofirmados en el almacén "raíz".</span><span class="sxs-lookup"><span data-stu-id="d6ad4-108">The user is prompted with a dialog box asking whether the user will accept self-signed certificates in the "Root" store.</span></span> <span data-ttu-id="d6ad4-109">Si el usuario acepta el certificado raíz, el resto de los certificados (excepto el certificado del solicitante) se colocan en el almacén de "CA".</span><span class="sxs-lookup"><span data-stu-id="d6ad4-109">If the user accepts the root certificate, the rest of the certificates (except for the requester's certificate) are placed in the "CA" store.</span></span> <span data-ttu-id="d6ad4-110">El certificado del solicitante se coloca en el almacén de certificados especificado por el solicitante en la propiedad [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .</span><span class="sxs-lookup"><span data-stu-id="d6ad4-110">The requester's certificate is placed in the certificate store specified by the requester in the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span>

<span data-ttu-id="d6ad4-111">En el ejemplo siguiente se muestra cómo usar el Visual Basic Scripting Edition (VBScript) y HTML en una página web para recibir y almacenar los certificados devueltos.</span><span class="sxs-lookup"><span data-stu-id="d6ad4-111">The following example shows how to use the Visual Basic Scripting Edition (VBScript) and HTML in a webpage to receive and store the returned certificates.</span></span>


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
