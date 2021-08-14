---
title: MCI_OPEN comando (Mmsystem.h)
description: El comando MCI \_ OPEN inicializa un dispositivo o archivo. Todos los dispositivos reconocen este comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN comando Windows Multimedia
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
ms.openlocfilehash: a84c95df35ecd602c207daa716b62d90f6bdc79b0ede7f937d3a38e6d6a9373b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689985"
---
# <a name="mci_open-command"></a>Comando MCI \_ OPEN

El comando MCI \_ OPEN inicializa un dispositivo o archivo. Todos los dispositivos reconocen este comando.

Para enviar este comando, llame a la [**función mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY o MCI \_ WAIT. Para obtener información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Puntero a una [**estructura MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) (Los dispositivos con conjuntos de comandos extendidos podrían reemplazar esta estructura por una estructura específica del dispositivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="remarks"></a>Comentarios

La marca MCI OPEN TYPE debe usarse siempre que se especifique un \_ dispositivo en la función \_ [**mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Si abre un dispositivo especificando una constante de tipo de dispositivo, debe especificar la marca MCI OPEN TYPE ID además \_ \_ de \_ MCI OPEN \_ \_ TYPE. Para obtener una lista de constantes de tipo de dispositivo, vea [Tipos de dispositivos MCI.](mci-device-types.md)

Si no se especifica la marca MCI OPEN SHAREABLE cuando se abre inicialmente un dispositivo o archivo, se producirá un error en todos los comandos MCI OPEN subsiguientes en el dispositivo o \_ \_ \_ archivo. Si el dispositivo o archivo ya está abierto y no se especifica esta marca, se producirá un error en la llamada aunque el primer comando open haya especificado MCI \_ OPEN \_ SHAREABLE. Archivos abiertos para MCISEQ. DRV y MCIWAVE. Los dispositivos DRV no pueden compartirse.

Case se omite en el nombre del dispositivo, pero no puede haber espacios en blanco iniciales o finales.

Para usar la selección automática de tipos (a través de las entradas del Registro), asigne el nombre de archivo y la extensión de archivo al miembro **lpstrElementName** de la estructura identificada por *lpOpen,* establezca el miembro **lpstrDeviceType** en **NULL** y establezca la marca \_ MCI OPEN \_ ELEMENT.

Las siguientes marcas adicionales se aplican a todos los dispositivos que admiten MCI \_ OPEN:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>ALIAS DE MCI \_ OPEN \_
</dt> <dd>

Se incluye un alias en el **miembro lpstrAlias** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ OPEN \_ SHAREABLE
</dt> <dd>

El dispositivo o archivo debe abrirse como compartible.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ OPEN \_ TYPE
</dt> <dd>

Se incluye un nombre de tipo de dispositivo o una constante en el **miembro lpstrDeviceType** de la estructura identificada *por lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI \_ OPEN \_ TYPE \_ ID
</dt> <dd>

La palabra de orden bajo del miembro **lpstrDeviceType** de la estructura identificada por *lpOpen* contiene un identificador de tipo de dispositivo MCI estándar y, opcionalmente, la palabra de orden superior contiene el índice ordinal del dispositivo. Use esta marca con la marca \_ MCI OPEN \_ TYPE.

</dd> </dl>

Las siguientes marcas adicionales se aplican a los dispositivos compuestos:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>ELEMENTO OPEN de MCI \_ \_
</dt> <dd>

Se incluye un nombre de archivo en el **miembro lpstrElementName** de la estructura identificada *por lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI \_ OPEN \_ ELEMENT \_ ID
</dt> <dd>

El **miembro lpstrElementName** de la estructura identificada por *lpOpen* se interpreta como un valor **DWORD** y tiene significado interno para el dispositivo. Use esta marca con la marca \_ MCI OPEN \_ ELEMENT.

</dd> </dl>

Las siguientes marcas adicionales se usan con el **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC
</dt> <dd>

El dispositivo debe reducir el número de colores estáticos (del sistema) en la paleta. Esto aumenta el número de colores disponibles para representar la secuencia de vídeo. Esta marca solo se aplica a los dispositivos que comparten una paleta con Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ OPEN \_ PARENT
</dt> <dd>

El identificador de ventana primaria se especifica en el **miembro hWndParent** de la estructura identificada *por lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ OPEN \_ WS
</dt> <dd>

Se especifica un estilo de ventana en el **miembro dwStyle** de la estructura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16BIT
</dt> <dd>

Indica una preferencia para la compatibilidad con dispositivos MCI de 16 bits.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ OPEN \_ 32BIT
</dt> <dd>

Indica una preferencia para la compatibilidad con dispositivos MCI de 32 bits.

</dd> </dl>

En el caso de los dispositivos de vídeo digital, el parámetro *lpOpen* apunta a una estructura [**MCI \_ DGV \_ OPEN \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)

Las siguientes marcas adicionales se usan con el tipo **de dispositivo superpuesto:**

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ OPEN \_ PARENT
</dt> <dd>

El identificador de ventana primaria se especifica en el **miembro hWndParent** de la estructura identificada *por lpOpen*.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ OPEN \_ WS
</dt> <dd>

Se especifica un estilo de ventana en el **miembro dwStyle** de la estructura identificada por *lpOpen*. El **valor dwStyle** especifica el estilo de la ventana que el controlador creará y mostrará si la aplicación no proporciona una. El parámetro style toma un entero que define el estilo de ventana. Estas constantes son las mismas que los estilos de ventana estándar (como WS \_ CHILD, WS \_ OVERLAPPEDWINDOW o WS \_ POPUP).

</dd> </dl>

En el caso de los dispositivos de superposición de vídeo, el parámetro *lpOpen* apunta a una estructura [**MCI \_ OVLY \_ OPEN \_ PARMS.**](mci-ovly-open-parms.md)

La siguiente marca adicional se usa con el **tipo de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>BÚFER ABIERTO \_ DE WAVE \_ DE MCI \_
</dt> <dd>

Se especifica una longitud de búfer en el **miembro dwBufferSeconds** de la estructura identificada por *lpOpen*.

</dd> </dl>

En el caso de los dispositivos de audio de forma de onda, el parámetro *lpOpen* apunta a una estructura [**\_ MCI WAVE \_ OPEN \_ PARMS.**](mci-wave-open-parms.md) El controlador MCIWAVE requiere un dispositivo asincrónico de audio y forma de onda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos de MCI](mci-commands.md)
</dt> </dl>

 

