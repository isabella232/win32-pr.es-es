---
description: Un campo de base de datos del tipo de datos FormattedSDDLText contiene una cadena de texto que describe un descriptor de seguridad mediante el lenguaje de definición de descriptor de seguridad (SDDL) válido. El campo SDDLText de la tabla MsiLockPermissionsEx usa este tipo de datos para proteger un objeto seleccionado. Tenga en cuenta que el campo SDDLText de la tabla MsiLockPermissionsEx no admite propiedades privadas o públicas.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ddfeac55f05ebea5f1603def6adcbac32aa9d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074753"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Un campo de base de datos del tipo de datos **FormattedSDDLText** contiene una cadena de texto que describe un descriptor de seguridad mediante el lenguaje de definición [de descriptor](../secauthz/security-descriptor-definition-language.md) de seguridad (SDDL) válido. El campo SDDLText de la tabla [MsiLockPermissionsEx](msilockpermissionsex-table.md) usa este tipo de datos para proteger un objeto seleccionado. Tenga en cuenta que el campo SDDLText de la tabla MsiLockPermissionsEx no admite propiedades privadas o públicas.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este tipo de datos está disponible a partir de Windows Installer 5.0.

El **tipo de datos FormattedSDDLText** puede contener una cadena SDDL escrita en formato de cadena de descriptor de seguridad [válido.](../secauthz/security-descriptor-string-format.md) Para obtener más información sobre SDDL, consulte [la Access Control](../secauthz/access-control.md) del Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)de Microsoft Windows. Además, una cadena de texto **FormattedSDDLText** puede usar corchetes angulares (<>) para contener el dominio y el nombre de usuario del usuario cuyo SID de cuenta se va a determinar.

Si el usuario que tiene el nombre de usuario *SampleUser* pertenece a un dominio denominado *SampleDomain*, el valor **FormattedSDDLText** puede identificar al propietario mediante la cadena SID, el nombre de usuario y el nombre de dominio, o las variables de entorno Windows. Por ejemplo, las cadenas siguientes serían posibles.

<dl> O:*cadena \_ de sid de \_ propietario* G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; *owner \_ sid \_ string*)(A;OICI;GA;;; BA)S:ARAI(AU; SEIAA;FA;;; WD)  
O:<*SampleDomain \\ SampleUser*>G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; <*SampleDomain \\ SampleUser*>)(A;OICI;GA;;; BA)S:ARAI(AU; SEIAA;FA;;; WD)  
O:<\[ %USERDOMAIN \] \\ \[ %USERNAME \]>G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; <\[ %USERDOMAIN \] \\ \[ %USERNAME \]>)(A;OICI;GA;;; BA)S:ARAI(AU; SEIAA;FA;;; WD)
</dl>

 

 
