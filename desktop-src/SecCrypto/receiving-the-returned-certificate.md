---
description: Explica cómo una aplicación recibe un certificado.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Recepción del certificado devuelto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476389"
---
# <a name="receiving-the-returned-certificate"></a>Recepción del certificado devuelto

Cuando la entidad de certificación (CA) ha comprobado la información de identidad del solicitante y se ha asegurado de que el solicitante es el propietario de la clave privada y que los datos sobre ese solicitante son precisos, la entidad de certificación crea un certificado X.509, lo firma y lo empaqueta con cualquier otro certificado necesario (por ejemplo, el propio certificado de la entidad de certificación) en un mensaje.  y envía el mensaje al solicitante. El mensaje puede ser un mensaje PKCS 7 o una respuesta de CMC (las plantillas V2 tienen como resultado \# una respuesta de CMC).

La aplicación receptora pasa el mensaje al Control de inscripción de certificados. A continuación, el Control de inscripción de certificados abre el mensaje y extrae los certificados. Se le pide al usuario un cuadro de diálogo que le pregunte si aceptará certificados autofirmados en el almacén "Raíz". Si el usuario acepta el certificado raíz, el resto de los certificados (excepto el certificado del solicitante) se colocan en el almacén "CA". El certificado del solicitante se coloca en el almacén de certificados especificado por el solicitante en la [**propiedad MyStoreName.**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename)

En el ejemplo siguiente se muestra cómo usar Visual Basic Scripting Edition (VBScript) y HTML en una página web para recibir y almacenar los certificados devueltos.


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



 

 
