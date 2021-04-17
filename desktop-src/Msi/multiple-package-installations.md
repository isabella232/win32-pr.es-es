---
description: Windows Installer puede instalar varios paquetes mediante el procesamiento de transacciones.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Instalaciones de Multiple-Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677659"
---
# <a name="multiple-package-installations"></a>Instalaciones de Multiple-Package

Windows Installer puede instalar varios paquetes mediante el [*procesamiento de transacciones*](t-gly.md). Esta funcionalidad está disponible a partir de Windows Installer 4,5. El instalador instalará todos los paquetes que pertenecen a una transacción de varios paquetes o ninguno de los paquetes. Si no se pueden instalar correctamente todos los paquetes de la transacción, o si el usuario cancela la instalación, el Windows Installer puede revertir los cambios y restaurar el equipo a su estado original.

Un paquete de instalación de varios paquetes puede contener una [tabla MsiEmbeddedChainer](msiembeddedchainer-table.md) que hace referencia a una función definida por el usuario que usa las funciones [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)y [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) .

En la [tabla MsiPackageCertificate](msipackagecertificate-table.md) se muestran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que realizan una instalación de varios paquetes. Puede usar esta tabla para reducir el número de veces que la instalación de varios paquetes muestra un mensaje de [*control de cuentas de usuario*](u-gly.md) (UAC) que requiere una respuesta por parte de un administrador.

Las siguientes funciones de Windows Installer pueden realizar cambios en el equipo del usuario cuando el Windows Installer instala, repara, actualiza o quita aplicaciones. A partir de Windows Installer 4,5, el instalador puede revertir los cambios realizados por estas funciones durante el [*procesamiento de transacciones*](t-gly.md) de una instalación de varios paquetes:

<dl>

[**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

Existe una excepción si el Windows Installer encuentra un paquete que pertenece a una instalación de varios paquetes que contiene una acción [ForceReboot](forcereboot-action.md) o [ScheduleReboot](schedulereboot-action.md) . En este caso, Windows Installer no instala solo ese paquete. Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes que no contengan una acción ForceReboot o ScheduleReboot.

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md): * * no se admite el [*procesamiento de transacciones*](t-gly.md) de instalaciones de Windows Installer de varios paquetes. Estas versiones de los Windows Installer no pueden revertir la instalación de varios paquetes como una sola transacción.

**Windows Server 2008 R2 con el rol de [servicios de escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No compatible. Se produce un error en una instalación de varios paquetes mediante la [tabla MsiEmbeddedChainer](msiembeddedchainer-table.md) si está habilitado el rol [servicios de escritorio remoto](../termserv/terminal-services-portal.md) .

 

 
