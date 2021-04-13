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
# <a name="init-method---cpapfile"></a>Método init: CPapFile

En el ejemplo de código siguiente se muestra cómo se inicializa **CPapFile** .

Este ejemplo es el método  **init** de **CPapFile** de Papfile. cpp.


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



El parámetro *pszAppFileName* se usa para inicializar CPapFile con un nombre de archivo predeterminado para las operaciones de carga o guardado posteriores. Se mantiene una copia en el miembro **m \_ szCurFileName** para la primera carga. En **StoClien**, este tipo de carga se intenta cuando la aplicación se inicia por primera vez después de que CPapFile se haya inicializado con *PSZAPPFILENAME* asignado "StoClien. PAP ". Este nombre de archivo se construyó en un constructor CGuiPaper obteniendo el nombre del módulo que se está ejecutando actualmente. (Se llama a la función [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) de Win32).

CPapFile requiere el parámetro *pIPaper* , porque usa esta interfaz en el objeto de copaper para realizar las operaciones de carga y guardado. Se llama a **AddRef** en esta copia almacenada de *pIPaper*, de acuerdo con las reglas com. Se llama a la **versión** coincidente en el destructor CPapFile.

 

 