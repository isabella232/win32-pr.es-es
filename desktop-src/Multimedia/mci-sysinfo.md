---
title: Comando MCI_SYSINFO (mmsystem. h)
description: El comando de MCI \_ SYSINFO recupera información acerca de los dispositivos MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Comando de MCI_SYSINFO de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996501"
---
# <a name="mci_sysinfo-command"></a>MCI \_ SYSINFO (comando)

El comando de MCI \_ SYSINFO recupera información acerca de los dispositivos MCI. MCI admite este comando directamente en lugar de pasarlo al dispositivo. Cualquier aplicación MCI puede usar este comando. La información de cadena se devuelve en el búfer proporcionado por la aplicación al que apunta el miembro **lpstrReturn** de la estructura identificada por *lpSysInfo*. La información numérica se devuelve como un valor **DWORD** colocado en el búfer proporcionado por la aplicación. El miembro **dwRetSize** especifica la longitud del búfer.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Una o varias de las siguientes marcas estándar y específicas del comando:

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI \_ SYSINFO \_ INSTALLNAME
</dt> <dd>

Obtiene el nombre (que aparece en el registro o en el archivo SYSTEM.INI) usado para instalar el dispositivo.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>nombre de MCI \_ SYSINFO \_
</dt> <dd>

Obtiene un nombre de dispositivo correspondiente al número de dispositivo especificado en el miembro **dwNumber** de la estructura identificada por **lpSysInfo**. Si \_ \_ se establece la marca de apertura de MCI SYSINFO, MCI devuelve los nombres de los dispositivos abiertos.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ SYSINFO \_ abierto
</dt> <dd>

Obtiene la cantidad o el nombre de los dispositivos abiertos.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>cantidad de MCI \_ SYSINFO \_
</dt> <dd>

Obtiene el número de dispositivos del tipo especificado que se enumeran en el registro o en la \[ \] sección MCI del archivo de SYSTEM.INI. Si \_ \_ se establece la marca de apertura de MCI SYSINFO, se devuelve el número de dispositivos abiertos.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de MCI SYSINFO**](mci-sysinfo-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

El miembro **wDeviceType** de la estructura identificada por *lpSysInfo* se usa para indicar el tipo de dispositivo de la consulta. Si el parámetro *wDeviceID* se establece en MCI \_ All \_ Device \_ ID, invalida el valor de **wDeviceType**. Para obtener una lista de tipos de dispositivos, consulte [tipos de dispositivos MCI](mci-device-types.md).

Los valores devueltos de tipo entero son valores **DWORD** devueltos en el búfer señalado por el miembro **lpstrReturn** de la estructura identificada por *lpSysInfo*.

Los valores devueltos de cadena son cadenas terminadas en NULL devueltas en el búfer señalado por el miembro **lpstrReturn** de la estructura identificada por *lpSysInfo*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

