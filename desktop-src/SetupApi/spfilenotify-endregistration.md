---
description: Cuando se usa la Directiva RegisterDlls INF para registrar automáticamente los archivos dll, los autores de la llamada de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registra o se anula su registro.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Mensaje de SPFILENOTIFY_ENDREGISTRATION (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669787"
---
# <a name="spfilenotify_endregistration-message"></a>SPFILENOTIFY \_ ENDREGISTRATION

Cuando se usa la directiva **RegisterDlls** inf para registrar automáticamente los archivos dll, los autores de la llamada de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registra o se anula su registro. Para enviar una notificación de **SPFILENOTIFY \_ ENDREGISTRATION** a una rutina de devolución de llamada una vez después de registrar o anular el registro de un archivo, incluya la más rotable \_ y \_ el marcador de rotación en el parámetro *Flags* de **SetupInstallFromInfSection**. Para enviar una notificación de anulación del registro, incluya \_ REGISTERCALLBACKAWARE más \_ de UNREGSVRs en el parámetro *Flags* .

La rutina de devolución de llamada especificada por el parámetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser el tipo de [devolución de \_ \_ llamada de archivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Establezca el parámetro de *contexto* en el mismo *contexto* especificado en **SetupInstallFromInfSection**. Establezca el parámetro de *notificación* en **SPFILENOTIFY \_ ENDREGISTRATION**.


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura de estado de control de registro de SP que contiene información sobre el archivo que se va a registrar o cuya registro se va a anular. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) El miembro **cbsize** debe establecerse en el tamaño de la estructura. **Filename** debe establecerse en la ruta de acceso completa del archivo que se va a registrar. **Win32Error** debe establecerse en un [código de error del sistema](/windows/desktop/Debug/system-error-codes) que indique un código de error extendido. **FailureCode** debe establecerse en uno de los códigos de error válidos que indican el resultado del registro. Para ver los códigos de error válidos, consulte [**Sp \_ Register \_ control \_ status**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).

</dd> <dt>

*Param2* 
</dt> <dd>

Si el archivo se está registrando, *parám2* debe establecerse en un puntero a un valor distinto de cero. Si se va a anular el registro del archivo, *parám2* debe establecerse en un puntero a cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl> | Detenga el procesamiento de la sección INF.<br/>     |
| <dl> <dt>**FILEOP \_ Doit**</dt> </dl>  | Continúe procesando la sección INF.<br/> |
| <dl> <dt>**\_Omitir archivo**</dt> </dl>    | Continuar procesando la sección INF<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



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

 

