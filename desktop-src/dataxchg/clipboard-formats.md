---
title: Formatos del Portapapeles
description: Una ventana puede colocar más de un objeto en el Portapapeles, cada uno de los que representa la misma información en un formato de Portapapeles diferente. Los usuarios no necesitan tener en cuenta los formatos del Portapapeles usados para un objeto en el Portapapeles.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- clipboard,formats
- clipboard,windows
- portapapeles, formatos estándar
- portapapeles, formatos registrados
- portapapeles, formatos sintetizados
- formatos estándar del Portapapeles
- formatos registrados del Portapapeles
- formatos de Portapapeles sintetizados
- formatos del Portapapeles en la nube
- formatos de historial del Portapapeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6bd2dc9dda8c8ccecd164123af68865005d9d28d328ce5489abf23926113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991345"
---
# <a name="clipboard-formats"></a>Formatos del Portapapeles

Una ventana puede colocar más de un objeto en el Portapapeles, cada uno de los que representa la misma información en un formato de Portapapeles diferente. Los usuarios no necesitan tener en cuenta los formatos del Portapapeles usados para un objeto en el Portapapeles.

En los temas siguientes se describen los formatos del Portapapeles.

-   [Formatos estándar del Portapapeles](#standard-clipboard-formats)
-   [Formatos registrados del Portapapeles](#registered-clipboard-formats)
-   [Formatos privados del Portapapeles](#private-clipboard-formats)
-   [Varios formatos de Portapapeles](#multiple-clipboard-formats)
-   [Formatos de Portapapeles sintetizados](#synthesized-clipboard-formats)
-   [Formatos de historial del Portapapeles y del Portapapeles en la nube](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Formatos estándar del Portapapeles

Los formatos del Portapapeles definidos por el sistema se denominan *formatos estándar del Portapapeles.* Estos formatos del Portapapeles se describen en [**Formatos estándar del Portapapeles**](standard-clipboard-formats.md).

## <a name="registered-clipboard-formats"></a>Formatos registrados del Portapapeles

Muchas aplicaciones funcionan con datos que no se pueden traducir a un formato estándar del Portapapeles sin pérdida de información. Estas aplicaciones pueden crear sus propios formatos de Portapapeles. Un formato del Portapapeles definido por una aplicación se denomina formato [registrado del Portapapeles](#registered-clipboard-formats). Por ejemplo, si una aplicación de procesamiento de palabras copia texto con formato en el Portapapeles con un formato de texto estándar, se perdería la información de formato. La solución sería registrar un nuevo formato del Portapapeles, como Formato de texto enriquecido (RTF).

Para registrar un nuevo formato del Portapapeles, use [**la función RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) Esta función toma el nombre del formato y devuelve un valor entero sin signo que representa el formato registrado del Portapapeles. Para recuperar el nombre del formato registrado del Portapapeles, pase el valor entero sin signo a la [**función GetClipboardFormatName.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea)

Si más de una aplicación registra un formato de Portapapeles exactamente con el mismo nombre, el formato del Portapapeles solo se registra una vez. Ambas llamadas a la [**función RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) devuelven el mismo valor. De esta manera, dos aplicaciones diferentes pueden compartir datos mediante un formato registrado del Portapapeles.

## <a name="private-clipboard-formats"></a>Formatos privados del Portapapeles

Una aplicación puede identificar un formato de Portapapeles privado definiendo un valor en el intervalo **CF \_ PRIVATEFIRST** a **CF \_ PRIVATELAST**. Una aplicación puede usar un formato de Portapapeles privado para un formato de datos definido por la aplicación que no es necesario registrar en el sistema.

El sistema no libera automáticamente los identificadores de datos asociados con formatos privados del Portapapeles. Si las ventanas usan formatos privados del Portapapeles, puede usar el mensaje [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) para liberar los recursos relacionados que ya no sean necesarios.

Para obtener más información sobre el [**mensaje \_ WM DESTROYCLIPBOARD,**](wm-destroyclipboard.md) vea [Clipboard Ownership](clipboard-operations.md).

Una aplicación puede colocar identificadores de datos en el Portapapeles definiendo un formato privado en el intervalo **CF \_ GDIOBJFIRST** a **CF \_ GDIOBJLAST**. Cuando se usan valores en este intervalo, el identificador de datos no es un identificador de un objeto Windows Interfaz de dispositivo gráfico (GDI), sino un identificador asignado por la [**función GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con la marca \_ GMEM MOVEABLE. Cuando se vacía el Portapapeles, el sistema elimina automáticamente el objeto mediante la [**función GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)

## <a name="multiple-clipboard-formats"></a>Varios formatos de Portapapeles

Una ventana puede colocar más de un objeto del Portapapeles en el Portapapeles, cada uno de los que representa la misma información en un formato de Portapapeles diferente. Al colocar información en el Portapapeles, la ventana debe proporcionar datos en tantos formatos como sea posible. Para averiguar cuántos formatos se usan actualmente en el Portapapeles, llame a la [**función CountClipboardFormats.**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats)

Los formatos del Portapapeles que contienen más información deben colocarse primero en el Portapapeles, seguidos de formatos menos descriptivos. Normalmente, una ventana que pega información del Portapapeles recupera un objeto del Portapapeles en el primer formato que reconoce. Dado que los formatos del Portapapeles se enumeran en el orden en que se colocan en el Portapapeles, el primer formato reconocido también es el más descriptivo.

Por ejemplo, suponga que un usuario copia texto con estilo de un documento de procesamiento de palabras. La ventana que contiene el documento podría colocar primero los datos en el Portapapeles en un formato registrado, como RTF. Posteriormente, la ventana colocaría los datos en el Portapapeles en un formato menos descriptivo, como texto **(CF \_ TEXT).**

Cuando el contenido del Portapapeles se pega en otra ventana, la ventana recupera los datos en el formato más descriptivo que reconoce. Si la ventana reconoce RTF, los datos correspondientes se pegan en el documento. De lo contrario, los datos de texto se pegan en el documento y se pierde la información de formato.

## <a name="synthesized-clipboard-formats"></a>Formatos de Portapapeles sintetizados

El sistema convierte implícitamente los datos entre determinados formatos del Portapapeles: si una ventana solicita datos en un formato que no está en el Portapapeles, el sistema convierte un formato disponible al formato solicitado. El sistema puede convertir datos como se indica en la tabla siguiente.



| Formato de Portapapeles     | Formato de conversión    |
|----------------------|----------------------|
| **MAPA DE BITS DE CF \_**       | **CF \_ DIB**          |
| **MAPA DE BITS DE CF \_**       | **CF \_ DIBV5**        |
| **CF \_ DIB**          | **MAPA DE BITS DE CF \_**       |
| **CF \_ DIB**          | **PALETA DE CF \_**      |
| **CF \_ DIB**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **MAPA DE BITS DE CF \_**       |
| **CF \_ DIBV5**        | **CF \_ DIB**          |
| **CF \_ DIBV5**        | **PALETA DE CF \_**      |
| **CF \_ ENHMETAFILE**  | **CF \_ METAFILEPICT** |
| **CF \_ METAFILEPICT** | **CF \_ ENHMETAFILE**  |
| **CF \_ OEMTEXT**      | **CF \_ TEXT**         |
| **CF \_ OEMTEXT**      | **CF \_ UNICODETEXT**  |
| **CF \_ TEXT**         | **CF \_ OEMTEXT**      |
| **CF \_ TEXT**         | **CF \_ UNICODETEXT**  |
| **CF \_ UNICODETEXT**  | **CF \_ OEMTEXT**      |
| **CF \_ UNICODETEXT**  | **CF \_ TEXT**         |



 

Si el sistema proporciona una conversión automática de tipos para un formato de Portapapeles determinado, no hay ninguna ventaja para colocar los formatos de conversión en el Portapapeles.

Si el sistema proporciona una conversión automática de tipos para un formato de Portapapeles determinado y llama a [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) para enumerar los formatos de datos del Portapapeles, el sistema enumera primero el formato que está en el Portapapeles, seguido de los formatos a los que se puede convertir.

Al copiar mapas de bits, es mejor colocar el formato **\_ CF DIB** o **CF \_ DIBV5** en el Portapapeles. Esto se debe a que los colores de un mapa de bits dependiente del dispositivo **(CF \_ BITMAP**) son relativos a la paleta del sistema, que puede cambiar antes de pegar el mapa de bits. Si el formato **\_ CF DIB** o **CF \_ DIBV5** está en el Portapapeles y una ventana solicita el formato CF **\_ BITMAP,** el sistema representa el mapa de bits independiente del dispositivo (DIB) mediante la paleta actual en ese momento.

Si coloca el formato DE MAPA DE **\_ BITS** de CF en el Portapapeles (y no **CF \_ DIB),** el sistema representa el formato del Portapapeles CF **\_ DIB** o **CF \_ DIBV5** en cuanto se cierra el Portapapeles. Esto garantiza que se usa la paleta correcta para generar la DIB. Si coloca el formato **\_ CF DIBV5** con la información del espacio de colores de mapa de bits en el Portapapeles, el sistema convertirá los bits de mapa de bits del espacio de colores del mapa de bits al espacio de colores sRGB cuando se solicite **CF \_ DIB** o **CF \_ DIBV5.** Si **se solicita CF \_ DIBV5** cuando no hay información de espacio de color en el Portapapeles, el sistema devuelve información de espacio de color sRGB en la estructura [**BITMAPV5HEADER.**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) Las conversiones entre otros formatos del Portapapeles se producen a petición.

Si el Portapapeles contiene datos en el formato **CF \_ PALETTE,** la aplicación debe usar las funciones [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) y [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) para realizar cualquier otro dato en el Portapapeles en esa paleta lógica.

Hay dos formatos del Portapapeles para los metarchivos: **CF \_ ENHMETAFILE** y **CF \_ METAFILEPICT**. Especifique **CF \_ ENHMETAFILE para** metarchivos mejorados y CF **\_ METAFILEPICT** para Windows metarchivos.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Formatos de historial de Portapapeles y Portapapeles en la nube

Algunas versiones de Windows incluyen [Cloud Clipboard,](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard)que mantiene un historial de los elementos de datos recientes del Portapapeles y puede sincronizarlos entre los dispositivos del usuario.
Si no desea que los datos que la aplicación coloque en el Portapapeles se incluyan en el historial del [](#registered-clipboard-formats) Portapapeles o se sincronicen con otros dispositivos, la aplicación puede controlar este comportamiento colocando datos en determinados formatos registrados del Portapapeles cuyos nombres conoce el sistema Windows:

- **ExcludeClipboardContentFromMonitorProcessing:** coloque los datos en el Portapapeles en este formato para evitar que todos los formatos del Portapapeles se incluyan en el historial del Portapapeles o se sincronicen con los demás dispositivos del usuario.
- **CanIncludeInClipboardHistory:** coloque un valor **[DWORD](../WinProg/windows-data-types.md)** serializado de cero en el Portapapeles en este formato para evitar que todos los formatos del Portapapeles se incluyan en el historial del Portapapeles, o bien coloque un valor de uno en su lugar para solicitar explícitamente que el elemento del Portapapeles se incluya en el historial del Portapapeles. Esto no afecta a la sincronización con los demás dispositivos del usuario.
- **CanUploadToCloudClipboard:** coloque un valor **[DWORD](../WinProg/windows-data-types.md)** serializado de cero en el Portapapeles en este formato para evitar que todos los formatos del Portapapeles se sincronicen con los demás dispositivos del usuario o coloque un valor de uno en su lugar para solicitar explícitamente que el elemento del Portapapeles se sincronice con otros dispositivos. Esto no afecta al historial del Portapapeles del dispositivo local.

Al igual que con otros formatos registrados del Portapapeles, deberá usar la función [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obtener un valor entero sin signo que identifique cada uno de los tres formatos anteriores.