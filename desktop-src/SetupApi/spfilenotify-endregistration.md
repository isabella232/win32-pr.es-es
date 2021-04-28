---
description: 'SPFILENOTIFY_ENDREGISTRATION mensaje: al usar la directiva REGISTERDlls INF para registrar automáticamente los archivos DLL, los autores de la llamada de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registran o anulan el registro.'
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: SPFILENOTIFY_ENDREGISTRATION mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec341c26f9f88390ff1b807e6e932b3b381cd57
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094513"
---
# <a name="spfilenotify_endregistration-message"></a>Mensaje SPFILENOTIFY \_ ENDREGISTRATION

Cuando se usa la directiva **REGISTERDlls** INF para registrar automáticamente los archivos DLL, los autores de la llamada de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registran o anulan el registro. Para enviar una notificación **SPFILENOTIFY \_ ENDREGISTRATION** a una rutina de devolución de llamada una vez después de registrar o anular el registro de un archivo, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST REGSVR en el parámetro \_ *Flags* de **SetupInstallFromInfSection**. Para enviar una notificación de anulación del registro, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST \_ UNREGSVR en el *parámetro Flags.*

La rutina de devolución de llamada especificada por el parámetro *MsgHandler* [**de SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser del tipo [PSP FILE \_ \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Establezca el *parámetro Context* en el mismo *contexto* especificado en **SetupInstallFromInfSection**. Establezca el *parámetro Notification* en **SPFILENOTIFY \_ ENDREGISTRATION**.


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) que contiene información sobre el archivo que se está registrando o anulando el registro. El **cbsize del** miembro debe establecerse en el tamaño de la estructura. **FileName** debe establecerse en la ruta de acceso completa del archivo que se va a registrar. **Win32Error debe** establecerse en un código [de error del sistema](/windows/desktop/Debug/system-error-codes) que indique un código de error extendido. **FailureCode** debe establecerse en uno de los códigos de error válidos que indican el resultado del registro. Para obtener códigos de error válidos, [**vea SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).

</dd> <dt>

*Param2* 
</dt> <dd>

Si el archivo se está registrando, *Param2* debe establecerse en un puntero a un valor distinto de cero. Si se anula el registro del archivo, *Param2* debe establecerse en un puntero a cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | Detenga el procesamiento de la sección INF.<br/>     |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Continúe procesando la sección INF.<br/> |
| <dl> <dt>**FILE \_ SKIP**</dt> </dl>    | Continuar procesando la sección INF<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)
</dt> </dl>

 

