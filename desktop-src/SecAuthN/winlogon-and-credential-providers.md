---
description: Es el módulo de Windows que realiza el inicio de sesión interactivo para una sesión de inicio de sesión. El comportamiento de Winlogon se puede personalizar implementando y registrando un proveedor de credenciales.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon y proveedores de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001083"
---
# <a name="winlogon-and-credential-providers"></a>Winlogon y proveedores de credenciales

[*Winlogon*](../secgloss/w-gly.md) es el módulo de Windows que realiza el inicio de sesión interactivo para una [*sesión de inicio*](../secgloss/l-gly.md)de sesión. El comportamiento de Winlogon se puede personalizar implementando y registrando un proveedor de credenciales.

Para obtener información acerca de la implementación de un proveedor de credenciales, vea los temas siguientes.



| Tema                                                                                                           | Descripción                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Experiencia de inicio de sesión Windows controlada por el proveedor de credenciales](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Información general de la arquitectura de los proveedores de credenciales y Winlogon y un proveedor de credenciales de ejemplo.<br/> |
| [Interfaces de Shell](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Referencia de la interfaz del proveedor de credenciales.<br/>                                                    |
| [Proveedores de credenciales en Windows 10](credential-providers-in-windows.md)<br/>                            | Proveedores de credenciales de terceros y proveedores de credenciales del sistema en Windows 10.<br/>             |



 

Para obtener una implementación de proveedor de credenciales de ejemplo, vea el ejemplo que se encuentra en el directorio de instalación de Windows SDK en \\ Samples \\ Security \\ CredentialProvider.

**Windows Server 2003 y Windows XP:** No se admiten proveedores de credenciales. Para obtener información acerca de cómo personalizar Winlogon, consulte [Winlogon y Gina](winlogon-and-gina.md).

 

 
