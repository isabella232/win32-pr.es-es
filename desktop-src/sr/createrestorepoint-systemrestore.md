---
title: Método CreateRestorePoint de la clase SystemRestore
description: Crea un punto de restauración.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Método CreateRestorePoint Restaurar sistema
- Método CreateRestorePoint Restaurar sistema, clase SystemRestore
- SystemRestore Class System Restore, CreateRestorePoint método
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491038"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a>Método CreateRestorePoint de la clase SystemRestore

Crea un punto de restauración.

Este método es el equivalente que admite scripts de la función [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descripción* \[ de de\]
</dt> <dd>

La descripción que se va a mostrar para que el usuario pueda identificar fácilmente un punto de restauración. La longitud máxima de una cadena ANSI es MAX \_ desc. La longitud máxima de una cadena Unicode es MAX \_ DESC \_ W. Para obtener más información, vea [texto de descripción de punto de restauración](restore-point-description-text.md).

</dd> <dt>

*RestorePointType* \[ de\]
</dt> <dd>

El tipo de punto de restauración. Este miembro puede ser uno de los valores siguientes.



| Tipo de punto de restauración                                                                                                                                                                                                                             | Significado                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Aplicación \_ de INSTALAR**</dt> <dt>0</dt> </dl>         | Se ha instalado una aplicación.<br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Aplicación \_ de Desinstalar**</dt> <dt>1</dt> </dl>   | Se ha desinstalado una aplicación.<br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Dispositivo \_ de \_Instalación del controlador**</dt> <dt>10</dt> </dl> | Se ha instalado un controlador de dispositivo.<br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Modificar \_ CONFIGURACIÓN**</dt> <dt>12</dt> </dl>                    | Una aplicación tiene características agregadas o eliminadas.<br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Cancelado \_ OPERACIÓN**</dt> <dt>13</dt> </dl>        | Una aplicación debe eliminar el punto de restauración que creó. Por ejemplo, una aplicación usaría esta marca cuando un usuario cancela una instalación.<br/> |



 

</dd> <dt>

*EventType* \[ de\]
</dt> <dd>

Tipo del evento. Este miembro puede ser uno de los valores siguientes.



| Tipo de evento                                                                                                                                                                                                                                                      | Significado                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Inicio \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>102</dt> </dl> | Ha empezado un cambio en el sistema. Una llamada subsiguiente anidada no crea un nuevo punto de restauración. <br/> Las llamadas subsiguientes deben usar END \_ Nested \_ System \_ Change, no end \_ System \_ Change.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Inicio \_ de \_Cambio del sistema**</dt> <dt>100</dt> </dl>                       | Ha empezado un cambio en el sistema. <br/> Una llamada subsiguiente debe usar el \_ cambio del sistema final \_ , no el \_ \_ cambio del sistema anidado \_ .<br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Fin \_ de Cambio de \_ sistema \_ anidado**</dt> <dt>103</dt> </dl>       | Ha finalizado un cambio de sistema.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Fin \_ de \_Cambio del sistema**</dt> <dt>101</dt> </dl>                             | Ha finalizado un cambio de sistema.<br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. De lo contrario, el método devuelve uno de los códigos de error COM definidos en WinError. h.

## <a name="remarks"></a>Observaciones

* * Windows 8: * *

Una nueva clave del registro permite a los desarrolladores de aplicaciones cambiar la frecuencia de creación de puntos de restauración.

Las aplicaciones deben crear esta clave para usarla, ya que no existirá en el sistema. De forma predeterminada, se aplicará lo siguiente si la clave no existe. Si una aplicación llama al método **CreateRestorePoint** para crear un punto de restauración, Windows omite la creación de este nuevo punto de restauración si se ha creado algún punto de restauración en las últimas 24 horas. El método **CreateRestorePoint** devuelve **S \_ correcto**.

Los desarrolladores pueden escribir aplicaciones que creen el valor **DWORD** **SystemRestorePointCreationFrequency** en la clave del registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. El valor de esta clave del registro puede cambiar la frecuencia de creación de puntos de restauración. El valor de esta clave del registro puede cambiar la frecuencia de creación de puntos de restauración.

Si la aplicación llama a **CreateRestorePoint** para crear un punto de restauración y el valor de la clave del registro es 0, Restaurar sistema no omite la creación del nuevo punto de restauración.

Si la aplicación llama a **CreateRestorePoint** para crear un punto de restauración y el valor de la clave del registro es el entero n, Restaurar sistema omite la creación de un nuevo punto de restauración si se crearon puntos de restauración en los N minutos anteriores.

## <a name="examples"></a>Ejemplos


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>MOF</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





