---
title: Métodos CGuiPaper
description: Los métodos de CGuiPaper se resumen de la siguiente manera. Todos estos métodos se implementan en GUIPAPER. CPP.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1303ca38ffe02da0dc747e1a8834d36419452209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773741"
---
# <a name="cguipaper-methods"></a>Métodos CGuiPaper

Los métodos de CGuiPaper se resumen de la siguiente manera. Todos estos métodos se implementan en GUIPAPER. CPP.



| Método                                                         | Descripción                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL init (HINSTANCE hInst, HWND hWnd, TCHAR \* pszCmdLineFile); | Inicializa el GuiPaper. Pide al servidor que cree un objeto de copaper.                                                     |
| HRESULT Drawon (void);                                          | Bloquea el papel para dibujar exclusivamente por este cliente.                                                                   |
| HRESULT DrawOff (void);                                         | Desbloquea el papel para permitir que se dibujen otros clientes.                                                                         |
| HRESULT ClearWin (void);                                        | Borra la ventana de presentación, pero conserva los datos de tinta.                                                                           |
| HRESULT PaintWin (void);                                        | Borra la ventana y vuelve a dibujar con los datos de entrada de lápiz actuales.                                                                     |
| Borrado HRESULT (void);                                           | Borra el contenido del dibujo actual y borra la ventana de presentación.                                                             |
| Cambiar el tamaño de HRESULT (WORD wWidth, WORD wHeight);                     | Cambia el tamaño de la ventana de presentación.                                                                                           |
| HRESULT InkWidth (SHORT nInkWidth);                             | Establece el ancho de la tinta actual para el dibujo.                                                                                   |
| HRESULT InkColor (COLORREF crInkColor);                         | Establece el color de la tinta actual para el dibujo.                                                                                   |
| HRESULT InkSaving (BOOL bInkSaving);                            | Activa y desactiva el almacenamiento de datos de tinta.                                                                          |
| HRESULT InkStart (SHORT nX, SHORT nY);                          | Inicia la secuencia de dibujo de tinta.                                                                                          |
| HRESULT InkDraw (SHORT nX, SHORT nY);                           | Dibuja datos de secuencia de entrada manuscrita.                                                                                              |
| HRESULT InkStop (SHORT nX, SHORT nY);                           | Detiene la secuencia de dibujo de tinta.                                                                                           |
| HRESULT ConnectPaperSink (void);                                | Conecta el objeto de PaperSink de cliente al origen de copapeles del servidor.                                                    |
| HRESULT DisconnectPaperSink (void);                             | Desconecte el objeto de PaperSink de cliente del origen de copapeles del servidor.                                                |
| Carga HRESULT (void);                                            | Carga los datos de tinta del archivo compuesto actual.                                                                            |
| HRESULT: guardar (void);                                            | Guarda los datos de tinta existentes en el archivo compuesto actual.                                                                     |
| HRESULT AskSave (void);                                         | Comprueba si el dibujo ha cambiado. En ese caso, muestra un cuadro de diálogo que pregunta al usuario si desea guardar los cambios y responde adecuadamente. |
| HRESULT Open (void);                                            | Muestra el cuadro de diálogo común de Win32. Abre el archivo compuesto de datos de papel existente.                                               |
| SaveAs de HRESULT (void);                                          | Muestra el cuadro de diálogo común de Win32. Guarda los datos del papel actual en el archivo cuyo nombre se ha cambiado.                                              |
| COLORREF PickColor (void);                                      | Muestra el cuadro de diálogo omunes de Win32. Pide al usuario que elija nuevo color de lápiz.                                                      |



 

El método **init** crea el objeto de copaper basado en servidor y asigna el miembro m PIPaper de CGuiPaper \_ .

Los métodos **AskSave**, **Open**, **SaveAs** y **PICKCOLOR** proporcionan un comportamiento familiar de la GUI mediante cuadros de diálogo comunes de Win32. Por ejemplo, el método **Open** usa el cuadro de diálogo Win32 Open File name para pedirle al usuario que especifique un nombre de archivo para abrirlo.

Los métodos **Load** y **Save** se tratarán en detalle más adelante en este paseo.

**InkSaving**, **InkStart**, **InkDraw** y **InkStop** son los métodos centrales para la funcionalidad de dibujo de la aplicación **StoClien** . **StoClien** usa estos métodos CGuiPaper para capturar, mostrar y almacenar los datos de dibujo interactivos tal y como se producen en el control de usuario. Realizan una función dual de dibujar la imagen dibujada en la ventana de cliente, así como de pasar los datos de dibujo a copapeles en el servidor. El copaper convierte los datos de dibujo en paquetes de datos de entrada de lápiz para su almacenamiento.

 

 




