---
description: Del mismo modo que una aplicación requiere un contexto de dispositivo de pantalla (DC) antes de que pueda empezar a dibujar en el área de cliente de una ventana, necesita un controlador de dominio de impresora antes de que pueda comenzar a enviar la salida a una impresora.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Contextos de dispositivo de impresora (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b75fb79d6ab8bb4198bf52bff10eccf5ec3cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277248"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Contextos de dispositivo de impresora (documentos e impresión)

Del mismo modo que una aplicación requiere un contexto de dispositivo de pantalla (DC) antes de que pueda empezar a dibujar en el área de cliente de una ventana, necesita un controlador de dominio de impresora antes de que pueda comenzar a enviar la salida a una impresora. Un controlador de dominio de impresora es similar a un controlador de dominio de pantalla, ya que es una estructura de datos interna que define un conjunto de objetos gráficos y sus atributos asociados y especifica los modos gráficos que afectan a la salida. Los objetos gráficos incluyen un lápiz para el dibujo de línea, un pincel para dibujar y rellenar, y una fuente para la salida de texto.

A diferencia de un controlador de dominio de pantalla, un controlador de dominio de impresora no es propiedad del componente de administración de ventanas y no se puede obtener llamando a la función [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) . En su lugar, una aplicación debe llamar a la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

Si la aplicación llama a la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , debe proporcionar un controlador y un nombre de puerto. Para recuperar estos nombres, llame a la función [**GetPrinter**](getprinter.md) o [**EnumPrinters**](enumprinters.md) .

Si la aplicación llama a la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) y especifica el \_ valor de PD RETURNDC en el miembro **Flags** de la estructura [**PrintDlgEx**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , el sistema devuelve un identificador a un contexto de dispositivo para la impresora seleccionada por el usuario. Para obtener más información, vea [Imprimir la hoja de propiedades](../dlgbox/print-property-sheet.md) y "usar la hoja de propiedades de impresión" en el tema sobre el uso de cuadros de [diálogo comunes](../dlgbox/using-common-dialog-boxes.md).

 

 
