---
title: Declaración de clase CGuiPaper
description: Declaración de clase CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068920"
---
# <a name="cguipaper-class-declaration"></a>Declaración de clase CGuiPaper

A continuación se muestra **la declaración de clase CGuiPaper** de GUIPAPER.H.


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



**CGuiPaper** mantiene las propiedades actuales de la GUI para el papel de dibujo. Los **miembros m \_ crInkColor**, **m \_ crInkWidth** y **m \_ WinRect** contienen valores para el color de la entrada de lápiz actual, el ancho de la entrada de lápiz y el rectángulo de dibujo. El **miembro m \_ hWnd** almacena el identificador en la ventana donde se realiza la pintura.

El dibujo real de las imágenes se realiza mediante un identificador para un contexto de dispositivo contenido en el **miembro m \_ hDC**. Un identificador del lápiz de dibujo actual se mantiene en el **miembro m \_ hPen**. El lápiz se destruye y se vuelve a crear cuando el usuario cambia su color o ancho.

Los **miembros m \_ pCOPaperSink** y **m \_ dwPaperSink** mantienen los valores necesarios para conectarse con COPaper para recibir notificaciones entrantes a través de la [**interfaz IPaperSink.**](ipapersink-methods.md) El **miembro m \_ bDirty** contiene una marca que indica que el usuario ha cambiado el dibujo y que ya no refleja los datos almacenados en su archivo.

El **miembro m \_ pIPaper** contiene el puntero de interfaz principal al objeto COPaper. A través de este puntero se accede a toda la funcionalidad de COPaper.

El **miembro m \_ nLockKey** se usa para admitir un esquema de bloqueo de cliente que se usa con varios clientes para permitir a un cliente acceso exclusivo a un objeto COPaper compartido. COPaper asigna **m \_ nLockKey** durante una llamada [**IPaper**](ipaper-methods.md)::**Lock** y el cliente pasa como parámetro en llamadas posteriores a COPaper. COPaper realizará el trabajo en esas llamadas solo si la clave de bloqueo que se pasa coincide con la clave que COPaper entregó por última vez a un cliente.

El **miembro m \_ pPapFile** contiene un puntero a un [**objeto CPapFile.**](cpapfile-class-and-methods.md) Es un objeto de C++ que encapsula las operaciones de carga y almacenamiento en un archivo compuesto de almacenamiento estructurado. **CPapFile funciona** con el objeto COPaper basado en servidor subyacente para cargar y guardar los datos de dibujo de COPaper.

 

 




