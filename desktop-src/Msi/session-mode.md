---
description: Esta es la propiedad Mode del objeto Session. Esta propiedad es un valor que representa la marca de modo designado para la sesión de instalación actual. La mayoría de las marcas de modo son de solo lectura externamente, pero también se pueden establecer algunas marcas especificadas.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Propiedad Session.Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed0c24280307cf368239ab88b5357924a3ee40d5a62444838e155aca2c0642f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629125"
---
# <a name="sessionmode-property"></a>Propiedad Session.Mode

Esta es la **propiedad Mode** del [**objeto Session.**](session-object.md) Esta propiedad es un valor que representa la marca de modo designado para la sesión de instalación actual. La mayoría de las marcas de modo son de solo lectura externamente, pero también se pueden establecer algunas marcas especificadas.

La [**función MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) devuelve un valor booleano TRUE o FALSE, lo que indica si la propiedad específica que se pasa a la función está establecida actualmente (TRUE) o no está establecida (FALSE).

Tenga en cuenta que no todos los valores de modo de ejecución de *flag* están disponibles al llamar a la propiedad **Mode** desde una acción personalizada diferida. Para obtener más información, vea Obtener información de contexto para acciones personalizadas [de ejecución aplazada.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a>Valor de propiedad

Valor entero requerido para la marca. Debe ser una de las siguientes:



| Nombre del marcador                                                                                                                                                                                                                                                                                                | Significado                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <dt>**msiRunModeAdmin**</dt> <dt>0</dt> </dl>                                              | Instalación en modo administrativo; de lo contrario, instalación del producto.<br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <dt>**msiRunModeAdvertise**</dt> <dt>1</dt> </dl>                              | Anuncia el modo de instalación.<br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <dt>**msiRunModeMaintenance**</dt> <dt>2</dt> </dl>                      | Base de datos en modo de mantenimiento cargada.<br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt> </dl>      | La reversión está habilitada.<br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <dt>**msiRunModeLogEnabled**</dt> <dt>4</dt> </dl>                          | El archivo de registro está activo.<br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <dt>**msiRunModeOperations**</dt> <dt>5</dt> </dl>                          | Ejecutar o ejecutar operaciones de cola.<br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt> </dl>                      | Es necesario reiniciar (configurable).<br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <dt>**msiRunModeRebootNow**</dt> <dt>7</dt> </dl>                              | Es necesario reiniciar para continuar con la instalación (configurable).<br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <dt>**msiRunModeCabinet**</dt> <dt>8</dt> </dl>                                      | Instalación de archivos desde archivadores y archivos mediante la tabla Multimedia.<br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt> </dl>  | Los archivos de origen solo usan nombres de archivo cortos.<br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt> </dl> | Los archivos de destino deben usar solo nombres de archivo cortos.<br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <dt>**msiRunModeWindows9x**</dt> <dt>12</dt> </dl>                             | El sistema operativo Windows 98/95.<br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <dt>**msiRunModeZawEnabled**</dt> <dt>13</dt> </dl>                         | El sistema operativo admite la publicidad de productos.<br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <dt>**msiRunModeScheduled**</dt> <dt>16</dt> </dl>                             | Acción personalizada [diferida llamada](custom-actions.md) desde la ejecución del script de instalación.<br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <dt>**msiRunModeRollback**</dt> <dt>17</dt> </dl>                                 | Acción personalizada [diferida llamada](custom-actions.md) desde el script de ejecución de reversión.<br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <dt>**msiRunModeCommit**</dt> <dt>18</dt> </dl>                                         | Acción personalizada [diferida llamada](custom-actions.md) desde el script de ejecución de confirmación.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



 

 




