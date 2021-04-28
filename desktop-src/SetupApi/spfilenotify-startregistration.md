---
description: 'SPFILENOTIFY_STARTREGISTRATION mensaje: al usar la directiva REGISTERDlls INF para registrar automáticamente archivos DLL, los llamadores de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registra o se anula el registro.'
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094503"
---
# <a name="spfilenotify_startregistration-message"></a>Mensaje DE SPFILENOTIFY \_ STARTREGISTRATION

Al usar la **directiva REGISTERDlls** INF para registrar automáticamente archivos DLL, los llamadores de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registra o se anula el registro. Para enviar una notificación **SPFILENOTIFY \_ STARTREGISTRATION** a la rutina de devolución de llamada una vez antes de registrar un archivo, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST REGSVR en el parámetro \_ *Flags* de **SetupInstallFromInfSection**. Para enviar una notificación de anulación del registro, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST UNREGSVR en el \_ *parámetro Flags.*

La rutina de devolución de llamada especificada por el parámetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser del tipo [PSP FILE \_ \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Establezca el *parámetro Context* en el mismo *contexto* especificado en **SetupInstallFromInfSection**. Establezca el *parámetro Notification* **en SPFILENOTIFY \_ STARTREGISTRATION**.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) que contiene información sobre el archivo que se está registrando o anulando el registro. El **cbsize del** miembro debe establecerse en el tamaño de la estructura . El **miembro FileName** debe establecerse en la ruta de acceso completa del archivo que se va a registrar. **Win32Error** no se usa y debe establecerse en NO \_ ERROR. **FailureCode** no se usa y debe establecerse en SPREG \_ SUCCESS.

</dd> <dt>

*Param2* 
</dt> <dd>

Si el archivo se está registrando, *Param2* debe establecerse en un puntero a un valor distinto de cero. Si se anula el registro del archivo, *Param2* debe establecerse en un puntero a cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.



| Código devuelto                                                                                  | Descripción                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ ABORT**</dt> </dl> | No registre ni desinscriba el archivo y detenga el procesamiento de la sección INF.<br/>             |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Registre o anula el registro del archivo y continúe procesando la sección INF.<br/>                |
| <dl> <dt>**FILE \_ SKIP**</dt> </dl>    | Omitir el registro o la anulación del registro del archivo, pero continuar procesando la sección INF<br/> |



 

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

[**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)
</dt> </dl>

 

