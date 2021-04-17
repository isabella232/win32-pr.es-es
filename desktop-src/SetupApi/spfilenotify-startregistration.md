---
description: Cuando se usa la Directiva RegisterDlls INF para registrar automáticamente los archivos dll, los autores de la llamada de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registra o se anula su registro.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Mensaje de SPFILENOTIFY_STARTREGISTRATION (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668171"
---
# <a name="spfilenotify_startregistration-message"></a>SPFILENOTIFY \_ STARTREGISTRATION

Cuando se usa la directiva **RegisterDlls** inf para registrar automáticamente los archivos dll, los autores de la llamada de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registra o se anula su registro. Para enviar una notificación de **SPFILENOTIFY \_ STARTREGISTRATION** a la rutina de devolución de llamada una vez antes de registrar un archivo, incluya \_ el bloque REGISTERCALLBACKAWARE más el marcador de giro \_ en el parámetro *Flags* de **SetupInstallFromInfSection**. Para enviar una notificación de anulación del registro, incluya \_ REGISTERCALLBACKAWARE más \_ de UNREGSVRs en el parámetro *Flags* .

La rutina de devolución de llamada especificada por el parámetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser el tipo de [devolución de \_ \_ llamada de archivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Establezca el parámetro de *contexto* en el mismo *contexto* especificado en **SetupInstallFromInfSection**. Establezca el parámetro de *notificación* en **SPFILENOTIFY \_ STARTREGISTRATION**.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Parámetro1* 
</dt> <dd>

Puntero a una estructura de estado de control de registro de SP que contiene información sobre el archivo que se va a registrar o cuya registro se va a anular. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) El miembro **cbsize** debe establecerse en el tamaño de la estructura. El miembro **filename** debe establecerse en la ruta de acceso completa del archivo que se va a registrar. **Win32Error** no se utiliza y debe establecerse en ningún \_ error. **FailureCode** no se utiliza y debe establecerse en SPREG \_ Success.

</dd> <dt>

*Param2* 
</dt> <dd>

Si el archivo se está registrando, *parám2* debe establecerse en un puntero a un valor distinto de cero. Si se va a anular el registro del archivo, *parám2* debe establecerse en un puntero a cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anulación de FILEOP**</dt> </dl> | No registre ni anule el registro del archivo y detenga el procesamiento de la sección INF.<br/>             |
| <dl> <dt>**FILEOP \_ Doit**</dt> </dl>  | Registre o anule el registro del archivo y continúe procesando la sección INF.<br/>                |
| <dl> <dt>**\_Omitir archivo**</dt> </dl>    | Omitir el registro o anular el registro del archivo, pero continuar procesando la sección INF<br/> |



 

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

[**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)
</dt> </dl>

 

