---
description: 'VSS permite la existencia de muchas instantáneas a la vez, pero solo permite que se encuentre en curso una creación de conjuntos de instantáneas entre la llamada a IVssBackupComponents:: StartSnapshotSet y la devolución de la llamada a IVssBackupComponents::D oSnapshotSet.'
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Control de errores en los proveedores de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f040526f63a0fe57fc5a49ac903e8b60b76646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653031"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Control de errores en los proveedores de instantáneas

VSS permite la existencia de muchas instantáneas a la vez, pero solo permite que se encuentre en curso una creación de conjuntos de instantáneas entre la llamada a [**ivssbackupcomponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) y la devolución de la llamada a [**Ivssbackupcomponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>No confirmaciones parciales

Si algún proveedor produce un error en una instantánea de cualquier volumen o LUN del conjunto de instantáneas, se produce un error en la creación del conjunto de instantáneas completo. es así por diseño. Este diseño simplifica los problemas de comportamiento asociados con la semántica de errores parciales y mantiene un momento dado coherente en todas las instantáneas del conjunto.

## <a name="reporting-fault-conditions"></a>Informes de condiciones de error

Si se produce un error o una condición de error del proveedor, el proveedor debe registrar un error en el registro de eventos de la aplicación. Esto incluye, entre otros, cualquier error específico del proveedor al crear o importar un conjunto de instantáneas, o un error de asignación de recursos para la instantánea de copia en escritura después de la creación. Este registro no debe realizarse durante el tiempo en el que los volúmenes del conjunto de instantáneas están en un estado inmovilizado.

## <a name="valid-provider-return-values"></a>Valores devueltos de proveedor válidos

En la tabla siguiente se enumeran los códigos de retorno válidos para los métodos de proveedor y su significado.



| Value                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ correcto<br/>                                                                                                                     | Método realizado correctamente.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OUTOFMEMORY<br/>                                                                                          | El proveedor no tiene memoria u otros recursos del sistema.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | Uno de los valores de parámetro no es válido.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ ACCESSDENIED<br/>                                                                                       | Un cliente sin privilegios ha intentado llamar al proveedor.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>Estado de VSS \_ E \_ incorrecto \_<br/>                                                                                  | Ningún proveedor es compatible con la operación solicitada o la operación no se puede realizar en el objeto porque el objeto no tiene el estado correcto.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>\_ \_ \_ no \_ se encontró el objeto de VSS E<br/>                                                            | Un parámetro hace referencia a un objeto que no se encontró (como un identificador de instantánea, un identificador de conjunto de instantáneas o un volumen).<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>\_ \_ almacenamiento insuficiente en VSS E \_<br/>                                                 | El proveedor no puede realizar la operación porque no hay suficiente espacio en disco.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>volumen de VSS \_ E \_ \_ no \_ compatible<br/>                                                | Ningún proveedor de este equipo admite la operación solicitada en el volumen.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>\_ \_ volumen de VSS E \_ no \_ compatible con el \_ \_ proveedor<br/>          | El proveedor no admite el volumen.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>se \_ \_ alcanzó el \_ número máximo \_ de \_ instantáneas de \_ VSS E<br/> | El proveedor ha alcanzado el número máximo de instantáneas que puede admitir.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>VETO de proveedor de VSS \_ E \_ \_<br/>                                                                      | El proveedor ha encontrado un error interno en tiempo de ejecución que no se asigna a otro valor devuelto. El proveedor también debe escribir un evento en el registro de eventos de aplicación que proporcione al usuario información sobre cómo resolver este problema.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E \_ no puede \_ revertir el \_ despatín<br/>                                                | No se pudo establecer la firma MBR o el ID. de GPT para uno o varios discos en el valor solicitado. Compruebe el registro de eventos de la aplicación para obtener más información.<br/>                                                                                            |



 

El proveedor no debe intentar devolver ningún otro código de error.

Si el proveedor devuelve un código de error que no se espera (por ejemplo, **S \_ false**, **e \_** **\_ inesperada** o **e \_ Abort**), VSS escribe un evento en el registro de eventos que menciona el proveedor y el método con errores y traduce el error en el error de **\_ \_ proveedor inesperado \_ \_ de VSS e** antes de volver al solicitante. Esto no se realiza para las devoluciones de [**IVssProviderCreateSnapshotSet:: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) o [**IVssProviderNotifications:: OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 




