---
description: Es el módulo Windows que realiza el inicio de sesión interactivo para una sesión de inicio de sesión. El comportamiento de Winlogon se puede personalizar implementando y registrando un Proveedor de credenciales.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Proveedores de winlogon y credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160883"
---
# <a name="winlogon-and-credential-providers"></a>Proveedores de winlogon y credenciales

[*Winlogon es*](../secgloss/w-gly.md) el módulo Windows que realiza el inicio de sesión interactivo para una [*sesión de inicio de sesión*](../secgloss/l-gly.md). El comportamiento de Winlogon se puede personalizar implementando y registrando un Proveedor de credenciales.

Para obtener información sobre cómo implementar una Proveedor de credenciales, vea los temas siguientes.



| Tema                                                                                                           | Descripción                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Proveedor de credenciales experiencia Windows inicio de sesión controlado](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Información general de Winlogon y Proveedor de credenciales arquitectura y un ejemplo de Proveedor de credenciales.<br/> |
| [Shell Interfaces](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Proveedor de credenciales de interfaz.<br/>                                                    |
| [Proveedores de credenciales en Windows 10](credential-providers-in-windows.md)<br/>                            | Proveedores de credenciales de terceros y proveedores de credenciales del sistema en Windows 10.<br/>             |



 

Para obtener un ejemplo Proveedor de credenciales implementación, consulte el ejemplo que se encuentra en el directorio de instalación del SDK de Windows en \\ Samples \\ Security \\ CredentialProvider(Ejemplos de CredentialProvider de seguridad).

**Windows Server 2003 y Windows XP:** No se admiten proveedores de credenciales. Para obtener información sobre cómo personalizar Winlogon, consulte [Winlogon y GINA.](winlogon-and-gina.md)

 

 
