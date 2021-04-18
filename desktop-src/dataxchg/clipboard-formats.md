---
title: Formatos del portapapeles
description: Una ventana puede colocar más de un objeto en el portapapeles, cada uno de los cuales representa la misma información en un formato de Portapapeles diferente. Los usuarios no necesitan tener en cuenta los formatos de Portapapeles utilizados para un objeto en el portapapeles.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- portapapeles, formatos
- portapapeles, Windows
- portapapeles, formatos estándar
- portapapeles, formatos registrados
- portapapeles, formatos sintetizados
- formatos de Portapapeles estándar
- formatos de Portapapeles registrados
- formatos de Portapapeles sintetizados
- formatos del portapapeles en la nube
- formatos de historial del portapapeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193ee4cc10c17846d974e50b17a464207026280b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714437"
---
# <a name="clipboard-formats"></a>Formatos del portapapeles

Una ventana puede colocar más de un objeto en el portapapeles, cada uno de los cuales representa la misma información en un formato de Portapapeles diferente. Los usuarios no necesitan tener en cuenta los formatos de Portapapeles utilizados para un objeto en el portapapeles.

En los temas siguientes se describen los formatos del portapapeles.

-   [Formatos de Portapapeles estándar](#standard-clipboard-formats)
-   [Formatos de Portapapeles registrados](#registered-clipboard-formats)
-   [Formatos de Portapapeles privados](#private-clipboard-formats)
-   [Varios formatos del portapapeles](#multiple-clipboard-formats)
-   [Formatos de Portapapeles sintetizados](#synthesized-clipboard-formats)
-   [Formatos de historial de Portapapeles y Portapapeles de nube](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Formatos de Portapapeles estándar

Los formatos del portapapeles definidos por el sistema se denominan *formatos estándar del portapapeles*. Estos formatos del portapapeles se describen en [**formatos estándar del portapapeles**](standard-clipboard-formats.md).

## <a name="registered-clipboard-formats"></a>Formatos de Portapapeles registrados

Muchas aplicaciones funcionan con datos que no se pueden traducir a un formato de Portapapeles estándar sin pérdida de información. Estas aplicaciones pueden crear sus propios formatos de Portapapeles. Un formato de Portapapeles definido por una aplicación se denomina [formato de Portapapeles registrado](#registered-clipboard-formats). Por ejemplo, si una aplicación de procesamiento de textos copia texto con formato en el Portapapeles con un formato de texto estándar, se perderá la información de formato. La solución sería registrar un nuevo formato del portapapeles, como el formato de texto enriquecido (RTF).

Para registrar un nuevo formato del portapapeles, utilice la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . Esta función toma el nombre del formato y devuelve un valor entero sin signo que representa el formato registrado del portapapeles. Para recuperar el nombre del formato registrado del portapapeles, pase el valor entero sin signo a la función [**GetClipboardFormatName**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea) .

Si más de una aplicación registra un formato de Portapapeles con exactamente el mismo nombre, el formato del portapapeles se registra una sola vez. Las dos llamadas a la función [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) devuelven el mismo valor. De esta manera, dos aplicaciones diferentes pueden compartir datos con un formato de Portapapeles registrado.

## <a name="private-clipboard-formats"></a>Formatos de Portapapeles privados

Una aplicación puede identificar un formato de Portapapeles privado definiendo un valor en el intervalo **CF \_ PRIVATEFIRST** a través de **CF \_ PRIVATELAST**. Una aplicación puede utilizar un formato de Portapapeles privado para un formato de datos definido por la aplicación que no es necesario registrar con el sistema.

El sistema no libera automáticamente los identificadores de datos asociados con los formatos de Portapapeles privados. Si las ventanas usan formatos privados del portapapeles, puede usar el mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) para liberar los recursos relacionados que ya no sean necesarios.

Para obtener más información sobre el mensaje de [**\_ DESTROYCLIPBOARD de WM**](wm-destroyclipboard.md) , consulte [propiedad del portapapeles](clipboard-operations.md).

Una aplicación puede colocar los identificadores de datos en el portapapeles definiendo un formato privado en el intervalo **CF \_ GDIOBJFIRST** a través de **CF \_ GDIOBJLAST**. Cuando se usan valores en este intervalo, el identificador de datos no es un identificador de un objeto de Windows Interfaz de dispositivo gráfico (GDI), sino un identificador asignado por la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con la \_ marca móvil GMEM. Cuando se vacía el portapapeles, el sistema elimina automáticamente el objeto mediante la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

## <a name="multiple-clipboard-formats"></a>Varios formatos del portapapeles

Una ventana puede colocar más de un objeto Clipboard en el portapapeles, cada uno de los cuales representa la misma información en un formato de Portapapeles diferente. Al colocar información en el portapapeles, la ventana debe proporcionar los datos en tantos formatos como sea posible. Para averiguar cuántos formatos se utilizan actualmente en el portapapeles, llame a la función [**CountClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) .

Los formatos del portapapeles que contienen la mayor parte de la información se deben colocar primero en el portapapeles, seguidos de formatos menos descriptivos. Una ventana que pega información del portapapeles normalmente recupera un objeto Clipboard en el primer formato que reconoce. Dado que los formatos del portapapeles se enumeran en el orden en el que se colocan en el portapapeles, el primer formato reconocido es también el más descriptivo.

Por ejemplo, supongamos que un usuario copia texto con estilo de un documento de procesamiento de texto. La ventana que contiene el documento puede colocar primero los datos en el portapapeles en un formato registrado, como RTF. Posteriormente, la ventana colocaría los datos en el portapapeles en un formato menos descriptivo, como texto (**CF \_ Text**).

Cuando el contenido del portapapeles se pega en otra ventana, la ventana recupera los datos en el formato más descriptivo que reconoce. Si la ventana reconoce RTF, los datos correspondientes se pegan en el documento. De lo contrario, los datos de texto se pegan en el documento y se pierde la información de formato.

## <a name="synthesized-clipboard-formats"></a>Formatos de Portapapeles sintetizados

El sistema convierte implícitamente los datos entre determinados formatos del portapapeles: Si una ventana solicita datos en un formato que no está en el portapapeles, el sistema convierte un formato disponible en el formato solicitado. El sistema puede convertir los datos como se indica en la tabla siguiente.



| Formato de Portapapeles     | Formato de conversión    |
|----------------------|----------------------|
| **mapa de bits de CF \_**       | **DIB de CF \_**          |
| **mapa de bits de CF \_**       | **CF \_ DIBV5**        |
| **DIB de CF \_**          | **mapa de bits de CF \_**       |
| **DIB de CF \_**          | **\_paleta CF**      |
| **DIB de CF \_**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **mapa de bits de CF \_**       |
| **CF \_ DIBV5**        | **DIB de CF \_**          |
| **CF \_ DIBV5**        | **\_paleta CF**      |
| **CF \_ ENHMETAFILE**  | **CF \_ METAFILEPICT** |
| **CF \_ METAFILEPICT** | **CF \_ ENHMETAFILE**  |
| **CF \_ OEMTEXT**      | **\_texto CF**         |
| **CF \_ OEMTEXT**      | **CF \_ UNICODETEXT**  |
| **\_texto CF**         | **CF \_ OEMTEXT**      |
| **\_texto CF**         | **CF \_ UNICODETEXT**  |
| **CF \_ UNICODETEXT**  | **CF \_ OEMTEXT**      |
| **CF \_ UNICODETEXT**  | **\_texto CF**         |



 

Si el sistema proporciona una conversión automática de tipos para un formato de Portapapeles determinado, no hay ninguna ventaja de colocar los formatos de conversión en el portapapeles.

Si el sistema proporciona una conversión automática de tipos para un formato de Portapapeles determinado y llama a [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) para enumerar los formatos de datos del portapapeles, el sistema primero enumera el formato que se encuentra en el portapapeles, seguido de los formatos a los que se puede convertir.

Al copiar mapas de bits, es mejor colocar el formato de **CF \_ DIB** o **CF \_ DIBV5** en el portapapeles. Esto se debe a que los colores de un mapa de bits dependiente del dispositivo (**\_ mapa de bits de CF**) son relativos a la paleta del sistema, que puede cambiar antes de pegar el mapa de bits. Si el formato de **CF \_ DIB** o **CF \_ DIBV5** está en el portapapeles y una ventana solicita el formato de **mapa de \_ bits de CF** , el sistema representa el mapa de bits independiente del dispositivo (DIB) con la paleta actual en ese momento.

Si coloca el formato **de \_ mapa de bits de CF** en el portapapeles (y no en **CF \_ DIB**), el sistema representa el formato del portapapeles de CF **\_ DIB** o **CF \_ DIBV5** en cuanto se cierre el portapapeles. Esto garantiza que se use la paleta correcta para generar el DIB. Si coloca el formato **CF \_ DIBV5** con la información del espacio de colores de mapa de bits en el portapapeles, el sistema convertirá los bits de mapa de bits del espacio de colores del mapa de bits en el espacio de color sRGB cuando se solicite **CF \_ DIB** o **CF \_ DIBV5** . Si se solicita **CF \_ DIBV5** cuando no hay información de espacio de colores en el portapapeles, el sistema devuelve información de espacio de color sRGB en la estructura [**BITMAPV5HEADER**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) . Las conversiones entre otros formatos del portapapeles se producen a petición.

Si el Portapapeles contiene datos en el formato de **\_ paleta de CF** , la aplicación debe usar las funciones [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) y [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) para realizar cualquier otro dato del portapapeles en la paleta lógica.

Hay dos formatos de Portapapeles para los metaarchivos: **CF \_ ENHMETAFILE** y **CF \_ METAFILEPICT**. Especifique **CF \_ ENHMETAFILE** para los metaarchivos mejorados y **CF \_ METAFILEPICT** para los metaarchivos de Windows.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Formatos de historial de Portapapeles y Portapapeles de nube

Algunas versiones de Windows incluyen el [portapapeles de la nube](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard), que mantiene un historial de los elementos de datos del portapapeles recientes y puede sincronizarlos entre los dispositivos del usuario.
Si no desea que los datos que la aplicación coloca en el portapapeles se incluyan en el historial del portapapeles o se sincronicen con otros dispositivos, la aplicación puede controlar este comportamiento colocando los datos en determinados [formatos del portapapeles registrados](#registered-clipboard-formats) cuyos nombres sean conocidos por el sistema de Windows:

- **ExcludeClipboardContentFromMonitorProcessing** : Coloque los datos en el portapapeles en este formato para evitar que todos los formatos del portapapeles se incluyan en el historial del portapapeles o se sincronicen con los demás dispositivos del usuario.
- **CanIncludeInClipboardHistory** : Coloque un valor **[DWORD](../WinProg/windows-data-types.md)** serializado de cero en el portapapeles en este formato para evitar que todos los formatos del portapapeles se incluyan en el historial del portapapeles, o bien Coloque un valor de uno para solicitar explícitamente que el elemento del portapapeles se incluya en el historial del portapapeles. Esto no afecta a la sincronización con los demás dispositivos del usuario.
- **CanUploadToCloudClipboard** : Coloque un valor **[DWORD](../WinProg/windows-data-types.md)** serializado de cero en el portapapeles en este formato para evitar que todos los formatos del portapapeles se sincronicen con los demás dispositivos del usuario o coloque un valor de uno para solicitar explícitamente que el elemento del portapapeles se sincronice con otros dispositivos. Esto no afecta al historial del Portapapeles del dispositivo local.

Al igual que con otros formatos de Portapapeles registrados, deberá usar la función [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obtener un valor entero sin signo que identifique cada uno de los tres formatos anteriores.