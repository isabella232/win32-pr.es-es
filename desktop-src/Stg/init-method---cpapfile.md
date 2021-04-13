---
title: 'Método init: CPapFile'
description: En el ejemplo de código siguiente se muestra cómo se inicializa CPapFile.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- 'Método init: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421190"
---
# <a name="init-method---cpapfile"></a><span data-ttu-id="49325-104">Método init: CPapFile</span><span class="sxs-lookup"><span data-stu-id="49325-104">Init Method - CPapFile</span></span>

<span data-ttu-id="49325-105">En el ejemplo de código siguiente se muestra cómo se inicializa **CPapFile** .</span><span class="sxs-lookup"><span data-stu-id="49325-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="49325-106">Este ejemplo es el método  **init** de **CPapFile** de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="49325-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



<span data-ttu-id="49325-107">El parámetro *pszAppFileName* se usa para inicializar CPapFile con un nombre de archivo predeterminado para las operaciones de carga o guardado posteriores.</span><span class="sxs-lookup"><span data-stu-id="49325-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="49325-108">Se mantiene una copia en el miembro **m \_ szCurFileName** para la primera carga.</span><span class="sxs-lookup"><span data-stu-id="49325-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="49325-109">En **StoClien**, este tipo de carga se intenta cuando la aplicación se inicia por primera vez después de que CPapFile se haya inicializado con *PSZAPPFILENAME* asignado "StoClien. PAP ".</span><span class="sxs-lookup"><span data-stu-id="49325-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="49325-110">Este nombre de archivo se construyó en un constructor CGuiPaper obteniendo el nombre del módulo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="49325-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="49325-111">(Se llama a la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) de Win32).</span><span class="sxs-lookup"><span data-stu-id="49325-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="49325-112">CPapFile requiere el parámetro *pIPaper* , porque usa esta interfaz en el objeto de copaper para realizar las operaciones de carga y guardado.</span><span class="sxs-lookup"><span data-stu-id="49325-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="49325-113">Se llama a **AddRef** en esta copia almacenada de *pIPaper*, de acuerdo con las reglas com.</span><span class="sxs-lookup"><span data-stu-id="49325-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="49325-114">Se llama a la **versión** coincidente en el destructor CPapFile.</span><span class="sxs-lookup"><span data-stu-id="49325-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 