---
description: Windows El instalador puede instalar varios paquetes mediante el procesamiento de transacciones.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Multiple-Package instalaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d525c2904d25fb06403f85914f2b04fce2ebc57f22801a2413b2f09ad1c396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943416"
---
# <a name="multiple-package-installations"></a>Multiple-Package instalaciones

Windows El instalador puede instalar varios paquetes mediante [*el procesamiento de transacciones.*](t-gly.md) Esta funcionalidad está disponible a partir de Windows Installer 4.5. El instalador instalará todos los paquetes que pertenecen a una transacción de varios paquetes o ninguno de los paquetes. Si todos los paquetes de la transacción no se pueden instalar correctamente, o si el usuario cancela la instalación, el instalador de Windows puede revertir los cambios y restaurar el equipo a su estado original.

Un paquete de instalación de varios paquetes puede contener una tabla [MsiEmbeddedChainer](msiembeddedchainer-table.md) que hace referencia a una función definida por el usuario que usa las funciones [**MsiBeginTransaction,**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)y [**MsiEndTransaction.**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)

En [la tabla MsiPackageCertificate se](msipackagecertificate-table.md) enumeran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen una instalación de varios paquetes. Puede usar esta tabla para reducir el número de veces que la instalación de varios paquetes muestra un mensaje de [*Control*](u-gly.md) de cuentas de usuario (UAC) que requiere una respuesta por parte de un administrador.

Las siguientes Windows installer pueden realizar cambios en el equipo del usuario cuando el instalador de Windows instala, repara, actualiza o quita aplicaciones. A partir Windows Installer 4.5, el instalador puede revertir los [](t-gly.md) cambios realizados por estas funciones durante el procesamiento de transacciones de una instalación de varios paquetes:

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

Hay una excepción si el instalador de Windows encuentra un paquete que pertenece a una instalación de varios paquetes que contiene una [acción ForceReboot](forcereboot-action.md) o [ScheduleReboot.](schedulereboot-action.md) En este caso, Windows instalador no instala solo ese paquete. Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes, que no contengan una acción ForceReboot o ScheduleReboot.

**[Windows Installer 4.0](not-supported-in-windows-installer-4-0.md)y versiones anteriores:[****](t-gly.md) No se admite el procesamiento de transacciones de varios paquetes Windows instalación del instalador. Estas versiones del instalador de Windows no pueden revertir la instalación de varios paquetes como una única transacción.

**Windows Server 2008 R2 con el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No se admite. Se produce un error en una instalación de varios paquetes mediante la tabla [MsiEmbeddedChainer](msiembeddedchainer-table.md) [si el rol](../termserv/terminal-services-portal.md) Servicios de Escritorio remoto está habilitado.

 

 
