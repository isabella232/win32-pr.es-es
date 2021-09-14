---
description: El método ProvideQualifiedComponent del objeto Installer devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria. Si es necesario, este método solicita el origen e incrementa el recuento de uso de la característica.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Método Installer.ProvideQualifiedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072101"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Método Installer.ProvideQualifiedComponent

El **método ProvideQualifiedComponent** del objeto [**Installer**](installer-object.md) devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria. Si es necesario, este método solicita el origen e incrementa el recuento de uso de la característica.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Categoría* 
</dt> <dd>

Especifica el identificador de componente para el componente solicitado. Puede que no sea el GUID del propio componente, sino un servidor que proporciona la funcionalidad correcta, como en la columna ComponentId de la [tabla PublishComponent](publishcomponent-table.md).

</dd> <dt>

*Calificador* 
</dt> <dd>

Especifica un calificador en una lista de componentes de publicidad (de [la tabla PublishComponent](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Define el modo de instalación. Este parámetro puede ser uno de los valores que se muestran en la tabla siguiente.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | Proporciona el componente , realizando cualquier instalación necesaria.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>–1</dt> </dl>                                                                            | Proporciona el componente solo si la característica existe; de lo contrario, devuelve una cadena vacía. Este modo comprueba la existencia del archivo de clave del componente.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt> </dl>                                                                | Proporciona el componente solo si la característica existe; de lo contrario, devuelve una cadena vacía. Este modo solo comprueba que el componente está registrado, pero no comprueba la existencia del archivo de clave del componente.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt> </dl>                                    | Proporciona la ruta de acceso del componente solo si la característica existe con un parámetro InstallState *de msiInstallStateLocal*. Esto comprueba el registro del componente, pero no comprueba la existencia del archivo de clave del componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinación de las marcas msiReinstallMode**</dt> <dt></dt> </dl> | Llama [**a ReinstallFeature**](installer-reinstallfeature.md) para volver a instalar la característica con este parámetro para el parámetro *ReinstallMode* y, a continuación, proporciona el componente .<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




