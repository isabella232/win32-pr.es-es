---
description: La propiedad FeatureState de solo lectura devuelve el estado instalado de una característica.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Installer.FeatureState, propiedad
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
ms.openlocfilehash: 989abe860848b943e77b02910e9760f8fcaecc97fd8a2634f8147605577613d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631279"
---
# <a name="installerfeaturestate-property"></a>Installer.FeatureState, propiedad

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
| msiInstallStateInvalidArg | Se pasó un parámetro no válido a la función . |
| msiInstallStateUnknown    | Se desconoce el código de producto o el identificador de característica.       |
| msiInstallStateBadConfig  | Los datos de configuración están dañados.               |



 

 

La **propiedad FeatureState** no valida que la característica sea accesible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




