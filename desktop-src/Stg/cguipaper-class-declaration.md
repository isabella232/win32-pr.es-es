---
title: Declaración de clase CGuiPaper
description: Declaración de clase CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075253"
---
# <a name="cguipaper-class-declaration"></a>Declaración de clase CGuiPaper

La siguiente es la declaración de clase **CGuiPaper** de GUIPAPER. H.


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



**CGuiPaper** mantiene las propiedades de la interfaz gráfica de usuario actual para el papel del dibujo. Los miembros **m \_ crInkColor**, **m \_ crInkWidth** y **m \_ WinRect** contienen valores para el color de tinta actual, el ancho de la tinta y el rectángulo del dibujo. El miembro del **\_ hWnd m** almacena el identificador en la ventana en la que se realiza el dibujo.

El dibujo real de imágenes se realiza mediante un identificador de un contexto de dispositivo que se encuentra en el miembro **m \_ HDC**. Un identificador del lápiz de dibujo actual se mantiene en el miembro **m \_ hPen**. El lápiz se destruye y se vuelve a crear cuando el usuario cambia el color o el ancho.

Los miembros **m \_ pCOPaperSink** y **m \_ dwPaperSink** contienen los valores necesarios para conectar con el copaper para recibir notificaciones entrantes a través de la interfaz [**IPaperSink**](ipapersink-methods.md) . El miembro **m \_ bDirty** contiene una marca que indica que el usuario ha cambiado el dibujo y que ya no refleja los datos almacenados en su archivo.

El miembro **m \_ pIPaper** contiene el puntero de interfaz principal al objeto de copaper. Se tiene acceso a todas las funciones de copaper a través de este puntero.

El miembro **m \_ nLockKey** se usa para admitir un esquema de bloqueo de cliente que se usa con varios clientes para permitir que un cliente tenga acceso exclusivo a un objeto de copaper compartido. El copaper asigna **m \_ nLockKey** durante una llamada a [**IPaper**](ipaper-methods.md)::**Lock** y se pasa como un parámetro por el cliente en llamadas posteriores a copapers. El copaper realizará el trabajo en esas llamadas solo si la tecla de bloqueo que se pasa coincide con la última entrega de la clave a un cliente mediante el copapel.

El miembro **m \_ pPapFile** contiene un puntero a un objeto [**CPapFile**](cpapfile-class-and-methods.md) . Es un objeto de C++ que encapsula las operaciones de carga y guardado en un archivo compuesto de almacenamiento estructurado. **CPapFile** funciona con el objeto de copaper subyacente basado en servidor para cargar y guardar los datos del dibujo de copapeles.

 

 




