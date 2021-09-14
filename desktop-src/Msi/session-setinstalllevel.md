---
description: El método SetInstallLevel del objeto Session establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los estados Select e Installed para todas las características de la tabla Feature.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Método Session.SetInstallLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272444"
---
# <a name="sessionsetinstalllevel-method"></a>Método Session.SetInstallLevel

El **método SetInstallLevel** del objeto [**Session**](session-object.md) establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los estados Select e Installed para todas las características de la tabla Feature. También establece el estado de acción de cada componente de la [tabla Componente](component-table.md) en función del nuevo nivel.

## <a name="syntax"></a>Sintaxis


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*installLevel* 
</dt> <dd>

Se requiere el nuevo nivel de instalación solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La [acción CostInitialize](costinitialize-action.md) debe ejecutarse antes de llamar a **SetInstallLevel**.

Si se pasa 0 para el parámetro *installLevel,* el nivel de instalación actual no cambia, pero todas las características se siguen actualizando en función del nivel de instalación actual. Por ejemplo, el módulo Controlador podría usar esta funcionalidad para restablecer todas las selecciones a sus estados predeterminados iniciales en cualquier momento del proceso de selección de la interfaz de usuario.

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




