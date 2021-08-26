---
description: VSS permite que existan muchas instantáneas a la vez, pero solo permite que la creación de un conjunto de instantáneas esté en curso entre la llamada a IVssBackupComponents::StartSnapshotSet y la devolución de la llamada a IVssBackupComponents::D oSnapshotSet.
ms.assetid: 26657fc2-180f-4ebb-820c-2159e7fe7584
title: Control de errores en proveedores de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0963df4c9c81c2cd9f96e7c1828243f3910a1df34d5ef94a714f17c57b404b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032685"
---
# <a name="error-handling-in-shadow-copy-providers"></a>Control de errores en proveedores de instantáneas

VSS permite que existan muchas instantáneas a la vez, pero solo permite que la creación de un conjunto de instantáneas esté en curso entre la llamada a [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) y la devolución de la llamada a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).

## <a name="no-partial-commit"></a>Sin confirmación parcial

Si algún proveedor produce un error en una instantánea en cualquier volumen o LUN del conjunto de instantáneas, se produce un error en la creación de todo el conjunto de instantáneas. es así por diseño. Este diseño simplifica los problemas de comportamiento asociados con la semántica de errores parciales y mantiene un punto en el tiempo coherente en todas las instantáneas del conjunto.

## <a name="reporting-fault-conditions"></a>Notificar condiciones de error

Si se produce un error de proveedor o una condición de error, el proveedor debe registrar un error en el registro de eventos de la aplicación. Esto incluye, entre otros, los errores específicos del proveedor al crear o importar un conjunto de instantáneas, o un error de asignación de recursos para la instantánea de copia en escritura después de la creación. Este registro no debe tener lugar durante el tiempo en que los volúmenes del conjunto de instantáneas se encuentran en estado inmovilizado.

## <a name="valid-provider-return-values"></a>Valores devueltos del proveedor válidos

En la tabla siguiente se enumeran los códigos de retorno válidos para los métodos de proveedor y sus significados.



| Value                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span>S \_ OK<br/>                                                                                                                     | Método realizado correctamente.<br/>                                                                                                                                                                                                                  |
| <span id="E_OUTOFMEMORY"></span><span id="e_outofmemory"></span>E \_ OUTOFMEMORY<br/>                                                                                          | El proveedor está sin memoria u otros recursos del sistema.<br/>                                                                                                                                                                                    |
| <span id="E_INVALIDARG"></span><span id="e_invalidarg"></span>E \_ INVALIDARG<br/>                                                                                             | Uno de los valores de parámetro no es válido.<br/>                                                                                                                                                                                                   |
| <span id="E_ACCESSDENIED"></span><span id="e_accessdenied"></span>E \_ ACCESSDENIED<br/>                                                                                       | Un cliente sin privilegios ha intentado llamar al proveedor.<br/>                                                                                                                                                                                |
| <span id="VSS_E_BAD_STATE"></span><span id="vss_e_bad_state"></span>ESTADO DE \_ VSS E \_ \_ BAD<br/>                                                                                  | Ningún proveedor admite la operación solicitada o la operación no se puede realizar en el objeto porque el objeto no está en el estado correcto.<br/>                                                                                     |
| <span id="VSS_E_OBJECT_NOT_FOUND"></span><span id="vss_e_object_not_found"></span>NO SE \_ ENCONTRÓ \_ EL OBJETO VSS \_ \_ E<br/>                                                            | Un parámetro hace referencia a un objeto que no se encontró (por ejemplo, un identificador de instantánea, un identificador de conjunto de instantáneas o un volumen).<br/>                                                                                                                               |
| <span id="VSS_E_INSUFFICIENT_STORAGE"></span><span id="vss_e_insufficient_storage"></span>ALMACENAMIENTO INSUFICIENTE DE VSS \_ E \_ \_<br/>                                                 | El proveedor no puede realizar la operación porque no hay suficiente espacio en disco.<br/>                                                                                                                                                           |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED"></span><span id="vss_e_volume_not_supported"></span>VOLUMEN VSS \_ E \_ NO \_ \_ COMPATIBLE<br/>                                                | Ningún proveedor de este equipo admite la operación solicitada en el volumen.<br/>                                                                                                                                                                |
| <span id="VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER"></span><span id="vss_e_volume_not_supported_by_provider"></span>VOLUMEN VSS \_ E NO COMPATIBLE CON EL \_ \_ \_ \_ \_ PROVEEDOR<br/>          | El proveedor no admite el volumen.<br/>                                                                                                                                                                                                   |
| <span id="VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED"></span><span id="vss_e_maximum_number_of_snapshots_reached"></span>NÚMERO MÁXIMO \_ DE INSTANTÁNEAS DE VSS E \_ \_ \_ \_ \_ ALCANZADO<br/> | El proveedor ha alcanzado el número máximo de instantáneas que puede admitir.<br/>                                                                                                                                                           |
| <span id="VSS_E_PROVIDER_VETO"></span><span id="vss_e_provider_veto"></span>VETO DEL PROVEEDOR DE VSS \_ \_ \_ E<br/>                                                                      | El proveedor ha encontrado un error interno en tiempo de ejecución que no se asigna a otro valor devuelto. El proveedor también debe escribir un evento en el registro de eventos de la aplicación para proporcionar al usuario información sobre cómo resolver este problema.<br/> |
| <span id="VSS_E_CANNOT_REVERT_DISKID"></span><span id="vss_e_cannot_revert_diskid"></span>VSS \_ E NO PUEDE REVERTIR \_ \_ \_ DISKID<br/>                                                | No se pudo establecer la firma de MBR o el identificador de GPT para uno o varios discos en el valor solicitado. Consulte el registro de eventos de la aplicación para obtener más información.<br/>                                                                                            |



 

El proveedor no debe intentar devolver ningún otro código de error.

Si el proveedor devuelve un código de error que no se espera (por **ejemplo, S \_ FALSE**, **E \_ FAIL**, **E \_ UNEXPECTED** o **E \_ ABORT),** VSS escribe un evento en el registro de eventos que menciona el proveedor y el método con errores y traduce el error a **VSS E UNEXPECTED PROVIDER \_ \_ \_ \_ ERROR** antes de volver al solicitante. Esto no se hace para las devoluciones de [**IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) o [**IVssProviderNotifications::OnUnload**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidernotifications-onunload).

 

 




