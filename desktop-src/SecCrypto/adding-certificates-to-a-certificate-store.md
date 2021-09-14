---
description: Los certificados se pueden agregar o quitar de los almacenes de certificados si el almacén se abre con permiso de lectura y escritura.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Agregar certificados a un almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173326"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Agregar certificados a un almacén de certificados

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

[*Los certificados*](../secgloss/c-gly.md) se pueden agregar o quitar de [*los*](../secgloss/c-gly.md) almacenes de certificados si el almacén se abre con permiso de lectura y escritura. El permiso de lectura y escritura no se concede a Active Directory almacenes. Aunque los certificados se pueden agregar o quitar de los almacenes de memoria, los cambios en los almacenes de memoria no se conservan entre sesiones.

Los certificados se pueden agregar a un almacén de certificados que se abre con permiso de lectura y escritura mediante el **método Add.** Un certificado se puede quitar de un almacén de certificados que se abre con permiso de lectura y escritura mediante el **método Remove.** Se pueden crear y guardar nuevas tiendas en las ubicaciones CAPICOM \_ CURRENT USER STORE y \_ \_ CAPICOM \_ LOCAL MACHINE \_ \_ STORE. Los almacenes recién creados en cualquiera de estas ubicaciones se pueden abrir con permiso de lectura y escritura.

En el ejemplo siguiente, se abren dos almacenes de certificados. Los certificados de los asuntos con apellidos que comienzan por F se recuperan del almacén Active Directory datos. A continuación, el ALMACÉN DE USUARIOS ACTUAL DE CAPICOM, el almacén DE CA DE CAPICOM se abre como un almacén de lectura y escritura y el primer certificado de la colección de certificados del almacén de Active Directory se agrega a los certificados del ALMACÉN DE CA \_ \_ \_ \_ \_ CAPICOM. \_ \_

Con fines de demostración, en el ejemplo se muestra la apertura de tiendas en las ubicaciones CAPICOM \_ MEMORY \_ STORE, CAPICOM CURRENT USER STORE y \_ \_ \_ CAPICOM \_ LOCAL MACHINE \_ \_ STORE. En el ejemplo se muestra la exportación de todos los certificados desde un almacén abierto, la escritura de los certificados exportados en un archivo, su lectura e importación en un almacén diferente. Los certificados recién importados se enumeran y se muestran.

En cualquier error CAPICOM, se devuelve un valor decimal negativo **de Err.Number.** Para obtener más información, [**vea CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obtener información sobre los valores decimales positivos de **Err.Number,** vea Winerror.h.

En el ejemplo siguiente se muestra cómo abrir almacenes de certificados mediante el enlace temprano en la declaración de los objetos **Store** y en la creación de una instancia de esos objetos.


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
