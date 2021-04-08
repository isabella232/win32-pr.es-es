---
description: Permita que las aplicaciones interactúen con el Módulo de plataforma segura (TPM) y el Cifrado de unidad BitLocker (BDE) mediante el marco de administración unificada de Instrumental de administración de Windows (WMI).
ms.assetid: acd1bc8e-3311-47f9-88b1-739f224e40e9
title: Acerca de los proveedores de WMI de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed75cebf14ee3eb419578111b7de15608661d91e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002585"
---
# <a name="about-security-wmi-providers"></a>Acerca de los proveedores de WMI de seguridad

Los proveedores de WMI de seguridad permiten a las aplicaciones interactuar con el Módulo de plataforma segura (TPM) y el Cifrado de unidad BitLocker (BDE) a través del marco de administración unificada de Instrumental de administración de Windows (WMI).



| Sección                                                                  | Descripción                                                                                                                    |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Referencia de proveedores de WMI de seguridad](security-wmi-providers-reference.md) | Documentación de la API para las clases [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) y [**Win32 \_ TPM**](win32-tpm.md) . |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

 

 
