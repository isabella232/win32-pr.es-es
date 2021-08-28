---
title: CPapFile (clase y métodos)
description: StoClien encapsula sus operaciones de archivo compuesto en un objeto CPapFile de C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36eaa46b9e675be2da699ed6f2fb0e2a2d8dd6db1e25cf0afba0f216f75a59e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962381"
---
# <a name="cpapfile-class-and-methods"></a>CPapFile (clase y métodos)

**StoClien** encapsula sus operaciones de archivo compuesto en un objeto CPapFile de C++.

A continuación se muestra **la declaración de clase CPapFile** de Papfile.h.


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



El objeto CPapFile mantiene un nombre de archivo actual en el **miembro m \_ szCurFileName**. Este nombre de archivo se usa como valor predeterminado en los métodos [**Load**](load-method---cpapfile.md) y [**Save**](save-method---cpapfile.md) cuando no reciben explícitamente un nombre de archivo.

Member **m \_ pIPaper** mantiene un puntero de interfaz a la interfaz COPaper [**IPaper.**](ipaper-methods.md) El **miembro m \_ pIStorage** mantiene un puntero a la [**interfaz IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del archivo compuesto actual que **StoClien** usa para el almacenamiento estructurado.

A continuación se muestra un resumen de los métodos de CPapFile.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




