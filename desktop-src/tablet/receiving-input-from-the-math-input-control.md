---
description: En esta sección se explica cómo recuperar el marcado de MathML desde el control de entrada matemática mediante el Active Template Library (ATL) y el modelo de objetos componentes (COM).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Recibir la entrada del control de entrada matemática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707142"
---
# <a name="receiving-input-from-the-math-input-control"></a>Recibir la entrada del control de entrada matemática

En esta sección se explica cómo recuperar el marcado de MathML desde el control de entrada matemática mediante el Active Template Library (ATL) y el modelo de objetos componentes (COM).

Para recuperar la ecuación matemática reconocida del control de entrada matemática, puede invalidar el comportamiento que se produce cuando se presiona el botón Insertar. Para ello, debe configurar un controlador de eventos que implemente los distintos eventos admitidos por la interfaz [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) . La configuración del controlador de eventos implica la realización de los siguientes pasos para los eventos que desea admitir (Inserte en este caso).

-   [Crear una clase de plantilla que contenga receptores de eventos](#create-a-template-class-that-contains-event-sinks)
-   [Configurar los controladores de eventos](#set-up-the-event-handlers)
-   [Heredar la clase de controlador de eventos en la clase principal](#inherit-the-event-handler-class-in-your-main-class)
-   [Inicialice la clase para heredar los receptores de eventos](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a>Crear una clase de plantilla que contenga receptores de eventos

Al implementar un receptor de eventos que usa el control de entrada matemática, primero debe especificar un identificador de receptor. A continuación, debe crear una clase de plantilla que herede de las interfaces de eventos de evento, de controlador de control de eventos y de control de entrada matemática. El código siguiente muestra cómo establecer un identificador de receptor y crear una clase de plantilla, CMathInputControlEventHandler, que hereda de las interfaces necesarias. Esta clase de plantilla también está configurada para tener un puntero de interfaz desconocido privado que se usará para pasar el control de entrada matemática a él en la inicialización y el \_ miembro m ulAdviseCount para contar el número de llamadas a Advise/Unadvise.


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> El miembro **m \_ pMain** debe ser diferente en su implementación si no está usando un cuadro de diálogo.

 

Ahora que tiene la clase de plantilla básica, debe proporcionar una declaración adelantada para los controladores de eventos que se van a reemplazar y, a continuación, debe configurar una asignación de receptor para los eventos que se van a controlar. En el código siguiente se muestra cómo configurar controladores de eventos para el método [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , al que se llama cuando un usuario hace clic en el botón Insertar del control de entrada matemática y el método [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , al que un usuario hace clic en el botón Cancelar del control de entrada matemática.


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



Dado que trabajará con el control de entrada matemática, será útil establecer una referencia interna a la interfaz correspondiente. La siguiente función de utilidad se crea en la clase de ejemplo para establecer esta referencia.


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a>Configurar los controladores de eventos

Una vez que haya configurado los receptores de eventos, tendrá que crear sus implementaciones de los receptores de eventos. En los dos métodos del ejemplo de código siguiente, los receptores de eventos recuperan un identificador de la interfaz de control de entrada matemática. En la función [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , el resultado del reconocimiento se muestra como MathML y el control está oculto. En la función [**cerrar**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , el control de entrada matemática está oculto.


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a>Heredar la clase de controlador de eventos en la clase principal

Una vez implementada la clase de plantilla, tendrá que heredarla en la clase en la que va a configurar el control de entrada matemática. Para los fines de esta guía, esta clase es un cuadro de diálogo, CMIC \_ Test \_ EVENTSDlg. En el encabezado del cuadro de diálogo, se deben incluir los encabezados necesarios y se debe heredar la clase de plantilla que creó. La clase que se va a heredar dentro de y los controladores de eventos deben tener declaraciones adelantadas para que se pueda implementar la plantilla. En el ejemplo de código siguiente se muestra cómo hacerlo.


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> El tipo de plantilla, **CMIC \_ Test \_ EventsDlg**, será diferente a menos que haya llamado a la clase igual que en el ejemplo.

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a>Inicialice la clase para heredar los receptores de eventos

Una vez configurada la clase para que herede de la clase de plantilla, está listo para configurarla para controlar eventos. Se compondrá de inicializar la clase para tener un identificador para el control de entrada matemática y la clase de llamada. Además, el control de entrada matemática para controlar los eventos de se debe enviar al método DispEventAdvise que la clase de ejemplo CMathInputControlEventHandler hereda. Se llama al siguiente código desde el método OnInitDialog de la clase de ejemplo para realizar estas acciones.


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> El tipo de plantilla CMIC \_ Test \_ EventsDlg en este ejemplo será diferente a menos que haya llamado a la clase igual que en el ejemplo.

 

 

 
