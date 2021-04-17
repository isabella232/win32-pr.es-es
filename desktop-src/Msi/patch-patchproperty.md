---
description: La propiedad PatchProperty obtiene información acerca de una revisión específica que se aplica a una instancia específica del producto. Esta propiedad llama a MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch. PatchProperty (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653750"
---
# <a name="patchpatchproperty-method"></a>Patch. PatchProperty (método)

La propiedad **PatchProperty** obtiene información acerca de una revisión específica que se aplica a una instancia específica del producto. Esta propiedad llama a [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

## <a name="syntax"></a>Sintaxis


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szProperty* 
</dt> <dd>

El parámetro *szProperty* puede tener uno de los valores siguientes.



| Nombre          | Significado                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | Obtiene el archivo de revisión almacenado en caché que usa el producto.                                                                                                                                                                                                                                                                               |
| Transformaciones    | Obtiene el conjunto de transformaciones de revisión aplicadas al producto en la última instalación de la revisión. Es posible que este valor no esté disponible para las aplicaciones por usuario no administradas si el usuario no ha iniciado sesión en el equipo.                                                                                                                     |
| InstallDate   | Obtiene la fecha en la que se aplicó la revisión al producto.                                                                                                                                                                                                                                                                      |
| No instalables | Devuelve "1" si la revisión está marcada como posible para la desinstalación del producto. En este caso, el instalador puede seguir bloqueando la desinstalación si esta revisión es necesaria para otra revisión que no se puede desinstalar.                                                                                                          |
| Estado         | Devuelve "1" si esta revisión se aplica actualmente al producto. Devuelve "2" si esta revisión se ha sustituido por otra revisión. Devuelve "4" si otra revisión ha hecho que esta revisión esté obsoleta. Estos valores corresponden a las constantes utilizadas por el parámetro *dwFilter* de [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa). |
| DisplayName   | Obtiene el nombre para mostrar registrado de la revisión. En el caso de las revisiones que no incluyen la propiedad DisplayName en la tabla [MsiPatchMetadata](msipatchmetadata-table.md) , el nombre para mostrar devuelto es una cadena vacía ("").                                                                                                      |
| MoreInfoURL   | Obtener la dirección URL de la información de soporte registrada para la revisión. En el caso de las revisiones que no incluyen la propiedad MoreInfoURL en la tabla [MsiPatchMetadata](msipatchmetadata-table.md) , la dirección URL de información de soporte devuelta es una cadena vacía ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método puede devolver ERROR \_ Unknown \_ patch si el objeto [**patch**](patch-object.md) se inicializa con una cadena vacía para *ProductCode*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Distribución**](patch-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




