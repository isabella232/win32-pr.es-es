---
description: El método SetInstallLevel del objeto de sesión establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los Estados Select e installed para todas las características de la tabla de características.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Método Session. SetInstallLevel
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653972"
---
# <a name="sessionsetinstalllevel-method"></a>Método Session. SetInstallLevel

El método **SetInstallLevel** del objeto de [**sesión**](session-object.md) establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los Estados Select e installed para todas las características de la tabla de características. También establece el estado de la acción de cada componente en la [tabla de componentes](component-table.md) basándose en el nuevo nivel.

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

Requerido nuevo nivel de instalación solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La [acción CostInitialize](costinitialize-action.md) debe ejecutarse antes de llamar a **SetInstallLevel**.

Si se pasa 0 para el parámetro *installLevel* , no se cambia el nivel de instalación actual, pero todas las características se siguen actualizando según el nivel de instalación actual. Por ejemplo, el módulo controlador podría usar esta funcionalidad para restablecer todas las selecciones a sus Estados predeterminados iniciales en cualquier momento del proceso de selección de la interfaz de usuario.

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




