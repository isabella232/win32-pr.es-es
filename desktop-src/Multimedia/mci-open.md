---
title: Comando MCI_OPEN (mmsystem. h)
description: El \_ comando MCI Open Inicializa un dispositivo o un archivo. Todos los dispositivos reconocen este comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Comando de MCI_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904980"
---
# <a name="mci_open-command"></a>\_Comando MCI Open

El \_ comando MCI Open Inicializa un dispositivo o un archivo. Todos los dispositivos reconocen este comando.

Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
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

\_Notificación de MCI o \_ espera de MCI. Para obtener información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Puntero a una [**estructura \_ \_ parms abierta de MCI**](mci-open-parms.md) . (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura con una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

La \_ marca MCI Open \_ Type se debe usar siempre que se especifique un dispositivo en la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Si abre un dispositivo mediante la especificación de una constante de tipo de dispositivo, debe especificar la \_ marca MCI Open \_ type id, además de \_ MCI \_ Open \_ Type. Para obtener una lista de las constantes de tipo de dispositivo, consulte [tipos de dispositivos MCI](mci-device-types.md).

Si \_ \_ no se especifica la marca MCI Open Shareable cuando se abre un dispositivo o un archivo inicialmente, se \_ producirá un error en todos los comandos abiertos de MCI posteriores al dispositivo o archivo. Si el dispositivo o el archivo ya están abiertos y no se especifica este marcador, se producirá un error en la llamada aunque el primer comando abierto especifique MCI \_ Open \_ Shareable. Archivos abiertos para MCISEQ. DRV y MCIWAVE. Los dispositivos DRV no se pueden compartir.

El caso se omite en el nombre del dispositivo, pero no puede haber espacios en blanco iniciales ni finales.

Para usar la selección automática de tipos (a través de las entradas del registro), asigne el nombre de archivo y la extensión de archivo al miembro **lpstrElementName** de la estructura identificada por *lpOpen*, establezca el miembro **lpstrDeviceType** en **null** y establezca la \_ marca de elemento abierto MCI \_ .

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ Open:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias abierto de MCI \_
</dt> <dd>

Un alias se incluye en el miembro **lpstrAlias** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ abierto \_ compartible
</dt> <dd>

El dispositivo o archivo debe abrirse como compartible.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_tipo abierto \_ MCI
</dt> <dd>

Un nombre de tipo de dispositivo o constante se incluye en el miembro **lpstrDeviceType** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ \_ ID. de tipo abierto MCI \_
</dt> <dd>

La palabra de orden inferior del miembro **lpstrDeviceType** de la estructura identificada por *lpOpen* contiene un identificador de tipo de dispositivo MCI estándar y la palabra de orden superior, opcionalmente, contiene el índice ordinal para el dispositivo. Use esta marca con la \_ marca MCI Open \_ Type.

</dd> </dl>

Las siguientes marcas adicionales se aplican a los dispositivos compuestos:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ Open ( \_ elemento)
</dt> <dd>

Un nombre de archivo se incluye en el miembro **lpstrElementName** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_identificador de \_ elemento \_ abierto MCI
</dt> <dd>

El miembro **lpstrElementName** de la estructura identificada por *lpOpen* se interpreta como un valor **DWORD** y tiene un significado interno en el dispositivo. Use esta marca con la \_ marca de \_ elemento abierto MCI.

</dd> </dl>

Con el tipo de dispositivo **DigitalVideo** se usan las siguientes marcas adicionales:

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ abrir \_ nostatic
</dt> <dd>

El dispositivo debe reducir el número de colores estáticos (del sistema) de la paleta. Esto aumenta el número de colores disponibles para representar la secuencia de vídeo. Esta marca solo se aplica a los dispositivos que comparten una paleta con Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ abrir \_ primario
</dt> <dd>

El identificador de ventana principal se especifica en el miembro **hWndParent** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ Open \_ WS
</dt> <dd>

Un estilo de ventana se especifica en el miembro **dwStyle** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>\_DGV de \_ \_ 16 bits de apertura de MCI
</dt> <dd>

Indica una preferencia para la compatibilidad con dispositivos MCI de 16 bits.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ Open \_ 32bit
</dt> <dd>

Indica una preferencia para la compatibilidad con dispositivos MCI de 32 bits.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpOpen* apunta a una estructura [**MCI \_ DGV \_ Open \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .

Se usan las siguientes marcas adicionales con el tipo de dispositivo **superpuesto** :

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ abrir \_ primario
</dt> <dd>

El identificador de ventana principal se especifica en el miembro **hWndParent** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ Open \_ WS
</dt> <dd>

Un estilo de ventana se especifica en el miembro **dwStyle** de la estructura identificada por *lpOpen*. El valor **dwStyle** especifica el estilo de la ventana que el controlador creará y mostrará si la aplicación no proporciona una. El parámetro Style toma un entero que define el estilo de la ventana. Estas constantes son las mismas que los estilos de ventana estándar (como WS \_ Child, WS \_ OVERLAPPEDWINDOW o WS \_ popup).

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpOpen* apunta a una estructura [**MCI \_ OVLY \_ Open \_ parms**](mci-ovly-open-parms.md) .

Con el tipo de dispositivo **WaveAudio** se usa la siguiente marca adicional:

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_ \_ búfer abierto de onda de MCI \_
</dt> <dd>

Se especifica una longitud de búfer en el miembro **dwBufferSeconds** de la estructura identificada por *lpOpen*.

</dd> </dl>

En el caso de los dispositivos de audio de onda, el parámetro *lpOpen* apunta a una estructura [**parms de MCI \_ \_ Open \_ Wave**](mci-wave-open-parms.md) . El controlador MCIWAVE requiere un dispositivo de audio de onda asincrónica.

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

 

