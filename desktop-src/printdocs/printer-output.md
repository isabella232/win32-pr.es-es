---
description: Del mismo modo que una aplicación requiere un contexto de dispositivo para mostrar (DC) antes de poder empezar a dibujar en el área cliente de una ventana, necesita un controlador de dominio de impresora antes de poder empezar a enviar la salida a una impresora.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Contextos de dispositivo de impresora (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c868d5bf8247375375b33bcb034a70bd6f28c5b9104b61e264543a63281069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947405"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Contextos de dispositivo de impresora (documentos e impresión)

Del mismo modo que una aplicación requiere un contexto de dispositivo para mostrar (DC) antes de poder empezar a dibujar en el área cliente de una ventana, necesita un controlador de dominio de impresora antes de poder empezar a enviar la salida a una impresora. Un controlador de dominio de impresora es similar a un controlador de dominio de presentación en que es una estructura de datos interna que define un conjunto de objetos gráficos y sus atributos asociados y especifica los modos gráficos que afectan a la salida. Los objetos gráficos incluyen un lápiz para dibujar líneas, un pincel para pintar y rellenar y una fuente para la salida de texto.

A diferencia de un controlador de dominio de presentación, un controlador de dominio de impresora no es propiedad del componente de administración de ventanas y no se puede obtener llamando a la [**función GetDC.**](/windows/desktop/api/winuser/nf-winuser-getdc) En su lugar, una aplicación debe llamar a [**la función CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o PrintDlgEx.**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))

Si la aplicación llama a [**la función CreateDC,**](/windows/desktop/api/wingdi/nf-wingdi-createdca) debe proporcionar un nombre de controlador y puerto. Para recuperar estos nombres, llame a [**la función GetPrinter**](getprinter.md) [**o EnumPrinters.**](enumprinters.md)

Si la aplicación llama a la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) y especifica el valor PD RETURNDC en el miembro Flags de la estructura \_ [**PRINTDLGEX,**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) el sistema devuelve un identificador a un contexto de dispositivo para la impresora seleccionada por el usuario.  Para obtener más información, vea [Imprimir hoja de propiedades](../dlgbox/print-property-sheet.md) y "Usar la hoja de propiedades de impresión" en Usar cuadros de diálogo [comunes](../dlgbox/using-common-dialog-boxes.md).

 

 
