---
description: La propiedad FeatureState de solo lectura devuelve el estado instalado de una característica.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Propiedad Installer. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653345"
---
# <a name="installerfeaturestate-property"></a>Propiedad Installer. FeatureState

La propiedad **FeatureState** de solo lectura devuelve el estado instalado de una característica.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve uno de los valores siguientes.



| Value                     | Descripción                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | La característica no está instalada.                    |
| msiInstallStateAdvertised | La característica se anuncia.                       |
| msiInstallStateLocal      | La característica se instala para ejecutarse localmente.         |
| msiInstallStateSource     | La característica se instala para ejecutarse desde el origen.     |
| msiInstallStateInvalidArg | Se pasó un parámetro no válido a la función. |
| msiInstallStateUnknown    | Se desconoce el código de producto o el ID. de característica.       |
| msiInstallStateBadConfig  | Los datos de configuración están dañados.               |



 

 

La propiedad **FeatureState** no valida que la característica sea accesible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




