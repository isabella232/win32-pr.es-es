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
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="035da-103">Recibir la entrada del control de entrada matemática</span><span class="sxs-lookup"><span data-stu-id="035da-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="035da-104">En esta sección se explica cómo recuperar el marcado de MathML desde el control de entrada matemática mediante el Active Template Library (ATL) y el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="035da-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="035da-105">Para recuperar la ecuación matemática reconocida del control de entrada matemática, puede invalidar el comportamiento que se produce cuando se presiona el botón Insertar.</span><span class="sxs-lookup"><span data-stu-id="035da-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="035da-106">Para ello, debe configurar un controlador de eventos que implemente los distintos eventos admitidos por la interfaz [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) .</span><span class="sxs-lookup"><span data-stu-id="035da-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="035da-107">La configuración del controlador de eventos implica la realización de los siguientes pasos para los eventos que desea admitir (Inserte en este caso).</span><span class="sxs-lookup"><span data-stu-id="035da-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="035da-108">Crear una clase de plantilla que contenga receptores de eventos</span><span class="sxs-lookup"><span data-stu-id="035da-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="035da-109">Configurar los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="035da-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="035da-110">Heredar la clase de controlador de eventos en la clase principal</span><span class="sxs-lookup"><span data-stu-id="035da-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="035da-111">Inicialice la clase para heredar los receptores de eventos</span><span class="sxs-lookup"><span data-stu-id="035da-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="035da-112">Crear una clase de plantilla que contenga receptores de eventos</span><span class="sxs-lookup"><span data-stu-id="035da-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="035da-113">Al implementar un receptor de eventos que usa el control de entrada matemática, primero debe especificar un identificador de receptor. A continuación, debe crear una clase de plantilla que herede de las interfaces de eventos de evento, de controlador de control de eventos y de control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="035da-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="035da-114">El código siguiente muestra cómo establecer un identificador de receptor y crear una clase de plantilla, CMathInputControlEventHandler, que hereda de las interfaces necesarias.</span><span class="sxs-lookup"><span data-stu-id="035da-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="035da-115">Esta clase de plantilla también está configurada para tener un puntero de interfaz desconocido privado que se usará para pasar el control de entrada matemática a él en la inicialización y el \_ miembro m ulAdviseCount para contar el número de llamadas a Advise/Unadvise.</span><span class="sxs-lookup"><span data-stu-id="035da-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


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
> <span data-ttu-id="035da-116">El miembro **m \_ pMain** debe ser diferente en su implementación si no está usando un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="035da-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="035da-117">Ahora que tiene la clase de plantilla básica, debe proporcionar una declaración adelantada para los controladores de eventos que se van a reemplazar y, a continuación, debe configurar una asignación de receptor para los eventos que se van a controlar.</span><span class="sxs-lookup"><span data-stu-id="035da-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="035da-118">En el código siguiente se muestra cómo configurar controladores de eventos para el método [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , al que se llama cuando un usuario hace clic en el botón Insertar del control de entrada matemática y el método [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , al que un usuario hace clic en el botón Cancelar del control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="035da-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="035da-119">Dado que trabajará con el control de entrada matemática, será útil establecer una referencia interna a la interfaz correspondiente.</span><span class="sxs-lookup"><span data-stu-id="035da-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="035da-120">La siguiente función de utilidad se crea en la clase de ejemplo para establecer esta referencia.</span><span class="sxs-lookup"><span data-stu-id="035da-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="035da-121">Configurar los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="035da-121">Set up the event handlers</span></span>

<span data-ttu-id="035da-122">Una vez que haya configurado los receptores de eventos, tendrá que crear sus implementaciones de los receptores de eventos.</span><span class="sxs-lookup"><span data-stu-id="035da-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="035da-123">En los dos métodos del ejemplo de código siguiente, los receptores de eventos recuperan un identificador de la interfaz de control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="035da-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="035da-124">En la función [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , el resultado del reconocimiento se muestra como MathML y el control está oculto.</span><span class="sxs-lookup"><span data-stu-id="035da-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="035da-125">En la función [**cerrar**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , el control de entrada matemática está oculto.</span><span class="sxs-lookup"><span data-stu-id="035da-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


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



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="035da-126">Heredar la clase de controlador de eventos en la clase principal</span><span class="sxs-lookup"><span data-stu-id="035da-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="035da-127">Una vez implementada la clase de plantilla, tendrá que heredarla en la clase en la que va a configurar el control de entrada matemática.</span><span class="sxs-lookup"><span data-stu-id="035da-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="035da-128">Para los fines de esta guía, esta clase es un cuadro de diálogo, CMIC \_ Test \_ EVENTSDlg.</span><span class="sxs-lookup"><span data-stu-id="035da-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="035da-129">En el encabezado del cuadro de diálogo, se deben incluir los encabezados necesarios y se debe heredar la clase de plantilla que creó.</span><span class="sxs-lookup"><span data-stu-id="035da-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="035da-130">La clase que se va a heredar dentro de y los controladores de eventos deben tener declaraciones adelantadas para que se pueda implementar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="035da-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="035da-131">En el ejemplo de código siguiente se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="035da-131">The following code example shows how this is done.</span></span>


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
> <span data-ttu-id="035da-132">El tipo de plantilla, **CMIC \_ Test \_ EventsDlg**, será diferente a menos que haya llamado a la clase igual que en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="035da-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="035da-133">Inicialice la clase para heredar los receptores de eventos</span><span class="sxs-lookup"><span data-stu-id="035da-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="035da-134">Una vez configurada la clase para que herede de la clase de plantilla, está listo para configurarla para controlar eventos.</span><span class="sxs-lookup"><span data-stu-id="035da-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="035da-135">Se compondrá de inicializar la clase para tener un identificador para el control de entrada matemática y la clase de llamada.</span><span class="sxs-lookup"><span data-stu-id="035da-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="035da-136">Además, el control de entrada matemática para controlar los eventos de se debe enviar al método DispEventAdvise que la clase de ejemplo CMathInputControlEventHandler hereda.</span><span class="sxs-lookup"><span data-stu-id="035da-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="035da-137">Se llama al siguiente código desde el método OnInitDialog de la clase de ejemplo para realizar estas acciones.</span><span class="sxs-lookup"><span data-stu-id="035da-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


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
> <span data-ttu-id="035da-138">El tipo de plantilla CMIC \_ Test \_ EventsDlg en este ejemplo será diferente a menos que haya llamado a la clase igual que en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="035da-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
