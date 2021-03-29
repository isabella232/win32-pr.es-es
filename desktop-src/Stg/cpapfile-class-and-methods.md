---
title: Clase y métodos de CPapFile
description: StoClien encapsula sus operaciones de archivo compuesto en un objeto CPapFile de C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994102"
---
# <a name="cpapfile-class-and-methods"></a>Clase y métodos de CPapFile

**StoClien** encapsula sus operaciones de archivo compuesto en un objeto CPapFile de C++.

La siguiente es la declaración de clase **CPapFile** de Papfile. h.


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



El objeto CPapFile mantiene un nombre de archivo actual en el miembro **m \_ szCurFileName**. Este nombre de archivo se utiliza como valor predeterminado en los métodos [**Load**](load-method---cpapfile.md) y [**Save**](save-method---cpapfile.md) cuando no reciben explícitamente un nombre de archivo.

El miembro **m \_ pIPaper** mantiene un puntero de interfaz a la interfaz [**IPaper**](ipaper-methods.md) de copaper. El miembro **m \_ pIStorage** mantiene un puntero a la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para el archivo compuesto actual que usa **StoClien** para el almacenamiento estructurado.

A continuación se encuentra un resumen de los métodos de CPapFile.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




