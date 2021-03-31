---
title: Comando MCI_LOAD (mmsystem. h)
description: El comando de carga de MCI \_ carga un archivo. Los dispositivos de vídeo digital y de superposición reconocen este comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Comando de MCI_LOAD de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995917"
---
# <a name="mci_load-command"></a>\_Comando carga de MCI

El comando de carga de MCI \_ carga un archivo. Los dispositivos de vídeo digital y de superposición reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

\_La notificación de MCI, la espera de MCI \_ o, para dispositivos de vídeo digital, la prueba de MCI \_ . Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms de carga de MCI**](mci-load-parms.md) . (Los dispositivos con parámetros adicionales podrían reemplazar esta estructura con una estructura específica del dispositivo. En el caso de los dispositivos de vídeo digital, el parámetro **lpLoad** apunta a una estructura [**DGV de \_ \_ carga \_ parms de MCI**](/previous-versions//dd743391(v=vs.85)) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La marca adicional siguiente se aplica a todos los dispositivos que admiten la carga de MCI \_ :

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_archivo de carga de MCI \_
</dt> <dd>

El miembro **lpfilename** de la estructura identificada por *lpLoad* contiene una dirección de un búfer que contiene el nombre de archivo.

</dd> </dl>

La siguiente marca adicional se usa con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect
</dt> <dd>

El miembro **RC** de la estructura identificada por *lpLoad* contiene un rectángulo de presentación válido que identifica el área del búfer de vídeo que se va a actualizar.

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpLoad* apunta a una estructura [**OVLY de carga de \_ \_ \_ parms MCI**](mci-ovly-load-parms.md) .

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

 

