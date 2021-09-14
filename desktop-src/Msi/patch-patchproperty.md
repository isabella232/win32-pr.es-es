---
description: La propiedad PatchProperty obtiene información sobre una revisión específica aplicada a una instancia específica del producto. Esta propiedad llama a MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Método Patch.PatchProperty
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173721"
---
# <a name="patchpatchproperty-method"></a>Método Patch.PatchProperty

La **propiedad PatchProperty** obtiene información sobre una revisión específica aplicada a una instancia específica del producto. Esta propiedad llama [**a MsiGetPatchInfoEx.**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)

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

El *parámetro szProperty* puede ser uno de los siguientes valores.



| Nombre          | Significado                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | Obtenga el archivo de revisión almacenado en caché que usa el producto.                                                                                                                                                                                                                                                                               |
| Transformaciones    | Obtenga el conjunto de transformaciones de revisión aplicadas al producto mediante la última instalación de revisión. Es posible que este valor no esté disponible para las aplicaciones no administradas por usuario si el usuario no ha iniciado sesión en el equipo.                                                                                                                     |
| InstallDate   | Obtenga la fecha en que se aplicó la revisión al producto.                                                                                                                                                                                                                                                                      |
| Desinstalable | Devuelve "1" si la revisión está marcada como posible para desinstalar del producto. En este caso, el instalador todavía puede bloquear la desinstalación si esta revisión es necesaria para otra revisión que no se puede desinstalar.                                                                                                          |
| State         | Devuelve "1" si esta revisión se aplica actualmente al producto. Devuelve "2" si esta revisión se ha reemplazado por otra revisión. Devuelve "4" si esta revisión se ha quedado obsoleta por otra revisión. Estos valores corresponden a las constantes utilizadas por el *parámetro dwFilter* [**de MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa). |
| DisplayName   | Obtenga el nombre para mostrar registrado de la revisión. Para las revisiones que no incluyen la propiedad DisplayName en la tabla [MsiPatchMetadata,](msipatchmetadata-table.md) el nombre para mostrar devuelto es una cadena vacía ("").                                                                                                      |
| MoreInfoURL   | Obtenga la dirección URL de información de soporte técnico registrada para la revisión. Para las revisiones que no incluyen la propiedad MoreInfoURL en la tabla [MsiPatchMetadata,](msipatchmetadata-table.md) la dirección URL de información de compatibilidad devuelta es una cadena vacía ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método puede devolver ERROR \_ UNKNOWN PATCH si el objeto \_ [**Patch**](patch-object.md) se inicializa con una cadena vacía para *ProductCode*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




