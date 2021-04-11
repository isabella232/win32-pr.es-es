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
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="afd3f-103">Declaración de clase CGuiPaper</span><span class="sxs-lookup"><span data-stu-id="afd3f-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="afd3f-104">La siguiente es la declaración de clase **CGuiPaper** de GUIPAPER. H.</span><span class="sxs-lookup"><span data-stu-id="afd3f-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


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



<span data-ttu-id="afd3f-105">**CGuiPaper** mantiene las propiedades de la interfaz gráfica de usuario actual para el papel del dibujo.</span><span class="sxs-lookup"><span data-stu-id="afd3f-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="afd3f-106">Los miembros **m \_ crInkColor**, **m \_ crInkWidth** y **m \_ WinRect** contienen valores para el color de tinta actual, el ancho de la tinta y el rectángulo del dibujo.</span><span class="sxs-lookup"><span data-stu-id="afd3f-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="afd3f-107">El miembro del **\_ hWnd m** almacena el identificador en la ventana en la que se realiza el dibujo.</span><span class="sxs-lookup"><span data-stu-id="afd3f-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="afd3f-108">El dibujo real de imágenes se realiza mediante un identificador de un contexto de dispositivo que se encuentra en el miembro **m \_ HDC**.</span><span class="sxs-lookup"><span data-stu-id="afd3f-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="afd3f-109">Un identificador del lápiz de dibujo actual se mantiene en el miembro **m \_ hPen**.</span><span class="sxs-lookup"><span data-stu-id="afd3f-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="afd3f-110">El lápiz se destruye y se vuelve a crear cuando el usuario cambia el color o el ancho.</span><span class="sxs-lookup"><span data-stu-id="afd3f-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="afd3f-111">Los miembros **m \_ pCOPaperSink** y **m \_ dwPaperSink** contienen los valores necesarios para conectar con el copaper para recibir notificaciones entrantes a través de la interfaz [**IPaperSink**](ipapersink-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="afd3f-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="afd3f-112">El miembro **m \_ bDirty** contiene una marca que indica que el usuario ha cambiado el dibujo y que ya no refleja los datos almacenados en su archivo.</span><span class="sxs-lookup"><span data-stu-id="afd3f-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="afd3f-113">El miembro **m \_ pIPaper** contiene el puntero de interfaz principal al objeto de copaper.</span><span class="sxs-lookup"><span data-stu-id="afd3f-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="afd3f-114">Se tiene acceso a todas las funciones de copaper a través de este puntero.</span><span class="sxs-lookup"><span data-stu-id="afd3f-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="afd3f-115">El miembro **m \_ nLockKey** se usa para admitir un esquema de bloqueo de cliente que se usa con varios clientes para permitir que un cliente tenga acceso exclusivo a un objeto de copaper compartido.</span><span class="sxs-lookup"><span data-stu-id="afd3f-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="afd3f-116">El copaper asigna **m \_ nLockKey** durante una llamada a [**IPaper**](ipaper-methods.md)::**Lock** y se pasa como un parámetro por el cliente en llamadas posteriores a copapers.</span><span class="sxs-lookup"><span data-stu-id="afd3f-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="afd3f-117">El copaper realizará el trabajo en esas llamadas solo si la tecla de bloqueo que se pasa coincide con la última entrega de la clave a un cliente mediante el copapel.</span><span class="sxs-lookup"><span data-stu-id="afd3f-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="afd3f-118">El miembro **m \_ pPapFile** contiene un puntero a un objeto [**CPapFile**](cpapfile-class-and-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="afd3f-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="afd3f-119">Es un objeto de C++ que encapsula las operaciones de carga y guardado en un archivo compuesto de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="afd3f-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="afd3f-120">**CPapFile** funciona con el objeto de copaper subyacente basado en servidor para cargar y guardar los datos del dibujo de copapeles.</span><span class="sxs-lookup"><span data-stu-id="afd3f-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




