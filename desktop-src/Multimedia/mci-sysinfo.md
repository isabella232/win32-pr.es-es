---
title: MCI_SYSINFO comando (Mmsystem.h)
description: El comando SYSINFO de MCI \_ recupera información sobre los dispositivos MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO comando Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370177"
---
# <a name="mci_sysinfo-command"></a>Comando \_ SYSINFO de MCI

El comando SYSINFO de MCI \_ recupera información sobre los dispositivos MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando. La información de cadena se devuelve en el búfer proporcionado por la aplicación al que apunta el **miembro lpstrReturn** de la estructura identificada por *lpSysInfo*. La información numérica se devuelve como **un valor DWORD** colocado en el búfer proporcionado por la aplicación. El **miembro dwRetSize** especifica la longitud del búfer.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

Una o varias de las siguientes marcas estándar y específicas de comandos:

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI \_ SYSINFO \_ INSTALLNAME
</dt> <dd>

Obtiene el nombre (que aparece en el registro o en SYSTEM.INI archivo) que se usa para instalar el dispositivo.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>NOMBRE \_ DE SYSINFO DE MCI \_
</dt> <dd>

Obtiene un nombre de dispositivo correspondiente al número de dispositivo especificado en el **miembro dwNumber** de la estructura identificada **por lpSysInfo**. Si se establece la \_ marca MCI SYSINFO \_ OPEN, MCI devuelve los nombres de los dispositivos abiertos.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ SYSINFO \_ OPEN
</dt> <dd>

Obtiene la cantidad o el nombre de los dispositivos abiertos.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>CANTIDAD \_ SYSINFO de MCI \_
</dt> <dd>

Obtiene el número de dispositivos del tipo especificado que aparecen en el Registro o en la sección mci del \[ \] archivo SYSTEM.INI especificado. Si se establece la \_ marca MCI SYSINFO \_ OPEN, se devuelve el número de dispositivos abiertos.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

Puntero a una [**estructura \_ MCI SYSINFO \_ PARMS.**](mci-sysinfo-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

El **miembro wDeviceType** de la estructura identificada por *lpSysInfo* se usa para indicar el tipo de dispositivo de la consulta. Si el *parámetro wDeviceID* se establece en MCI ALL DEVICE ID, invalida el \_ valor de \_ \_ **wDeviceType.** Para obtener una lista de los tipos de dispositivo, vea [Tipos de dispositivo de MCI.](mci-device-types.md)

Los valores devueltos de enteros son **valores DWORD** devueltos en el búfer al que apunta el **miembro lpstrReturn** de la estructura identificada por *lpSysInfo*.

Los valores devueltos de cadena son cadenas terminadas en null devueltas en el búfer al que apunta el **miembro lpstrReturn** de la estructura identificada por *lpSysInfo*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 

