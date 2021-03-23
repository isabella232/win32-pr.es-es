---
title: Enlaces en DirectML
description: En DirectML, el enlace hace referencia a los datos adjuntos de los recursos a la canalización para que la GPU los use durante la inicialización y la ejecución de los operadores de aprendizaje automático.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: a04bf0bcc63fff810604e3db72fe507cc10040f5
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104549118"
---
# <a name="binding-in-directml"></a>Enlaces en DirectML

En DirectML, el *enlace* hace referencia a los datos adjuntos de los recursos a la canalización para que la GPU los use durante la inicialización y la ejecución de los operadores de aprendizaje automático. Estos recursos pueden ser, por ejemplo, los de entrada y salida, así como los recursos temporales o persistentes que necesita el operador.

En este tema se tratan los detalles conceptuales y procedimentales del enlace. Se recomienda leer completamente la documentación de las API a las que llama, incluidos los parámetros y las notas.

## <a name="important-ideas-in-binding"></a>Ideas importantes en el enlace

La lista de pasos siguientes contiene una descripción de alto nivel de las tareas relacionadas con el enlace. Debe seguir estos pasos cada vez que [ejecute un redistribuible](/windows/desktop/api/directml/nn-directml-idmldispatchable), &mdash; un reenviador es un inicializador de operador o un operador compilado. En estos pasos se presentan las ideas, estructuras y métodos importantes implicados en el enlace DirectML.

Las secciones siguientes de este tema profundizan y explican con más detalle estas tareas de enlace, con fragmentos de código ilustrativos tomados del ejemplo de código de la [aplicación DirectML mínima](dml-min-app.md) .

- Llame a [**IDMLDispatchable:: GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) en el distribuidor para determinar cuántos descriptores necesita y también sus necesidades de recursos temporales o persistentes.
- Cree un montón de descriptores de Direct3D 12 lo suficientemente grande para los descriptores y enlácelo a la canalización.
- Llame a [**IDMLDevice:: CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) para crear una tabla de enlace de DirectML que represente los recursos enlazados a la canalización. Utilice la estructura [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) para describir la tabla de enlace, incluido el subconjunto de los descriptores a los que apunta en el montón de descriptores.
- Cree recursos temporales o persistentes como recursos de búfer de Direct3D 12, los describe con [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) y [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) estructuras y agréguelos a la tabla de enlace.
- Si el distribuidor es un operador compilado, cree un búfer de elementos tensores como un recurso de búfer de Direct3D 12. Rellénelo o cárguelo, describa el **DML_BUFFER_BINDING** y **DML_BINDING_DESC** estructuras y agréguelo a la tabla de enlace.
- Pase la tabla de enlace como un parámetro al llamar a [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

## <a name="retrieve-the-binding-properties-of-a-dispatchable"></a>Recuperar las propiedades de enlace de un reenviador

En la estructura de [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties) se describen las necesidades de enlace de un operador que se debe reenviar (inicializador de operador o compilado). Estas propiedades relacionadas con el enlace incluyen el número de descriptores que se deben enlazar al distribuidor, así como el tamaño en bytes de cualquier recurso temporal o persistente que necesite.

> [!NOTE]
> Incluso en el caso de varios operadores del mismo tipo, no realice suposiciones sobre ellos que tengan los mismos requisitos de enlace. Consulte las propiedades de enlace para cada inicializador y operador que cree.

Llame a [**IDMLDispatchable:: GetBindingProperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) para recuperar un **DML_BINDING_PROPERTIES**.

```cppwinrt
winrt::com_ptr<::IDMLCompiledOperator> dmlCompiledOperator;
// Code to create and compile a DirectML operator goes here.

DML_BINDING_PROPERTIES executeDmlBindingProperties{
    dmlCompiledOperator->GetBindingProperties()
};

winrt::com_ptr<::IDMLOperatorInitializer> dmlOperatorInitializer;
// Code to create a DirectML operator initializer goes here.

DML_BINDING_PROPERTIES initializeDmlBindingProperties{
    dmlOperatorInitializer->GetBindingProperties()
};

UINT descriptorCount = ...
```

El `descriptorCount` valor que se recupera aquí determina el tamaño (mínimo) del montón descriptor y la tabla de enlace que se crea en los dos pasos siguientes.

**DML_BINDING_PROPERTIES** también contiene un `TemporaryResourceSize` miembro, que es el tamaño mínimo, en bytes, del recurso temporal que se debe enlazar a la tabla de enlace para este objeto que se puede distribuir. Un valor de cero significa que no se requiere un recurso temporal.

Y un `PersistentResourceSize` miembro, que es el tamaño mínimo, en bytes, del recurso persistente que se debe enlazar a la tabla de enlace para este objeto que se puede distribuir. Un valor de cero significa que no se requiere un recurso persistente. Se debe proporcionar un recurso persistente, si es necesario, durante la inicialización de un operador compilado (donde se enlaza como salida del inicializador de operador), así como durante la ejecución. Hay más información sobre esto más adelante en este tema. Solo los operadores compilados tienen recursos persistentes: los inicializadores de operador siempre devuelven un valor de 0 para este miembro.

Si llama a **IDMLDispatchable:: GetBindingProperties** en un inicializador de operador tanto antes como después de una llamada a [**IDMLOperatorInitializer:: RESET**](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset), no se garantiza que los dos conjuntos de propiedades de enlace recuperadas sean idénticos.

## <a name="describe-create-and-bind-a-descriptor-heap"></a>Describir, crear y enlazar un montón de descriptores

En lo que respecta a los descriptores, su responsabilidad comienza y termina con el montón del descriptor. DirectML se encarga de la creación y administración de los descriptores dentro del montón que se proporciona.

Por lo tanto, use una estructura de [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) para describir un montón lo suficientemente grande como para el número de descriptores que necesita el distribuidor. A continuación, créelo con [**ID3D12Device:: CreateDescriptorHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap). Y, por último, llame a [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) para enlazar el montón de descriptores a la canalización.

```cppwinrt
winrt::com_ptr<::ID3D12DescriptorHeap> d3D12DescriptorHeap;

D3D12_DESCRIPTOR_HEAP_DESC descriptorHeapDescription{};
descriptorHeapDescription.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
descriptorHeapDescription.NumDescriptors = descriptorCount;
descriptorHeapDescription.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;

winrt::check_hresult(
    d3D12Device->CreateDescriptorHeap(
        &descriptorHeapDescription,
        _uuidof(d3D12DescriptorHeap),
        d3D12DescriptorHeap.put_void()
    )
);

std::array<ID3D12DescriptorHeap*, 1> d3D12DescriptorHeaps{ d3D12DescriptorHeap.get() };
d3D12GraphicsCommandList->SetDescriptorHeaps(
    static_cast<UINT>(d3D12DescriptorHeaps.size()),
    d3D12DescriptorHeaps.data()
);
```

## <a name="describe-and-create-a-binding-table"></a>Describir y crear una tabla de enlace

Una tabla de enlace de DirectML representa los recursos que se enlazan a la canalización para que los utilice un distribuidor. Esos recursos podrían ser los de entrada y salida (u otros parámetros) para un operador, o bien pueden ser varios recursos persistentes y temporales con los que funciona un distribuidor.

Use la estructura [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) para describir la tabla de enlace, incluido el distribuidor para el que la tabla de enlace representará los enlaces y el intervalo de descriptores (del montón de descriptores que acaba de crear) al que desea que haga referencia la tabla de enlace (y en el que DirectML puede escribir descriptores). El `descriptorCount` valor (una de las propiedades de enlace que se recuperaron en el primer paso) nos indica qué tamaño mínimo es, en descriptores, de la tabla de enlace necesaria para el objeto que se debe enviar. En este caso, usamos ese valor para indicar el número máximo de descriptores que DirectML puede escribir en nuestro montón, desde el inicio de los controladores de la CPU y del descriptor de GPU suministrados.

Después, llame a [**IDMLDevice:: CreateBindingTable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) para crear la tabla de enlace DirectML. En pasos posteriores, después de haber creado más recursos para el distribuidor, agregaremos esos recursos a la tabla de enlace.

En lugar de pasar una **DML_BINDING_TABLE_DESC** a esta llamada, puede pasar `nullptr` , que indica una tabla de enlace vacía.

```cppwinrt
DML_BINDING_TABLE_DESC dmlBindingTableDesc{};
dmlBindingTableDesc.Dispatchable = dmlOperatorInitializer.get();
dmlBindingTableDesc.CPUDescriptorHandle = d3D12DescriptorHeap->GetCPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.GPUDescriptorHandle = d3D12DescriptorHeap->GetGPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.SizeInDescriptors = descriptorCount;

winrt::com_ptr<::IDMLBindingTable> dmlBindingTable;
winrt::check_hresult(
    dmlDevice->CreateBindingTable(
        &dmlBindingTableDesc,
        __uuidof(dmlBindingTable),
        dmlBindingTable.put_void()
    )
);
```

El orden en el que DirectML escribe descriptores en el montón no está especificado, por lo que la aplicación debe tener cuidado de no sobrescribir los descriptores ajustados por la tabla de enlace. Los identificadores de descriptor de CPU y de GPU proporcionados pueden provienen de montones diferentes; sin embargo, es responsabilidad de la aplicación asegurarse de que todo el intervalo de descriptor al que hace referencia el identificador del descriptor de CPU se copia en el intervalo al que hace referencia el identificador de descriptor de GPU antes de la ejecución mediante esta tabla de enlace El montón descriptor desde el que se proporcionan los identificadores debe tener el tipo **D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV**. Además, el montón al que hace referencia `GPUDescriptorHandle` debe ser un montón de descriptores visible del sombreador.

Puede restablecer una tabla de enlace para quitar todos los recursos que haya agregado a ella, al mismo tiempo que cambia cualquier propiedad establecida en su **DML_BINDING_TABLE_DESC** inicial (para encapsular un nuevo intervalo de descriptores o para volver a utilizarlo para otro que se pueda enviar). Solo tiene que realizar los cambios en la estructura de la descripción y llamar a [**IDMLBindingTable:: RESET**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset).

```cppwinrt
dmlBindingTableDesc.Dispatchable = pIDMLCompiledOperator.get();

winrt::check_hresult(
    pIDMLBindingTable->Reset(
        &dmlBindingTableDesc
    )
);
```

## <a name="describe-and-bind-any-temporarypersistent-resources"></a>Describir y enlazar los recursos temporales o persistentes

La estructura de **DML_BINDING_PROPERTIES** que hemos rellenado al [recuperar las propiedades de enlace](#retrieve-the-binding-properties-of-a-dispatchable) de nuestro redistribuible contiene el tamaño en bytes de cualquier recurso temporal o persistente que necesite el distribuidor. Si alguno de estos tamaños es distinto de cero, cree un recurso de búfer de Direct3D 12 y agréguelo a la tabla de enlace.

En el ejemplo de código siguiente, se crea un recurso temporal ( `temporaryResourceSize` bytes de tamaño) para el que se pudo enviar. Se describe cómo se desea enlazar el recurso y, después, se agrega ese enlace a la tabla de enlace.

Como estamos enlazando un único recurso de búfer, se describe nuestro enlace con una estructura de [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) . En esa estructura, se especifica el recurso de búfer de Direct3D 12 (el recurso debe tener [**D3D12_RESOURCE_DIMENSION_BUFFER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)de dimensión), así como un desplazamiento y tamaño en el búfer. También es posible describir un enlace para una matriz de búferes (en lugar de para un único búfer) y la estructura de [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding) existe para ese propósito.

Para abstraer la distinción entre un enlace de búfer y un enlace de matriz de búfer, usamos la estructura de  [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) . Puede establecer el `Type` miembro del **DML_BINDING_DESC** en [**DML_BINDING_TYPE_BUFFER**](/windows/desktop/api/directml/ne-directml-dml_binding_type) o **DML_BINDING_TYPE_BUFFER_ARRAY**. Además, puede establecer el `Desc` miembro para que apunte a un **DML_BUFFER_BINDING** o a un **DML_BUFFER_ARRAY_BINDING**, dependiendo de `Type` .

Estamos tratando con el recurso temporal en este ejemplo, por lo que lo agregaremos a la tabla de enlace con una llamada a [**IDMLBindingTable:: BindTemporaryResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource).

```cppwinrt
D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
winrt::com_ptr<::ID3D12Resource> temporaryBuffer;

D3D12_RESOURCE_DESC temporaryBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(temporaryResourceSize) };
winrt::check_hresult(
    d3D12Device->CreateCommittedResource(
        &defaultHeapProperties,
        D3D12_HEAP_FLAG_NONE,
        &temporaryBufferDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        __uuidof(temporaryBuffer),
        temporaryBuffer.put_void()
    )
);

DML_BUFFER_BINDING bufferBinding{ temporaryBuffer.get(), 0, temporaryResourceSize };
DML_BINDING_DESC bindingDesc{ DML_BINDING_TYPE_BUFFER, &bufferBinding };
dmlBindingTable->BindTemporaryResource(&bindingDesc);
```

Un recurso temporal (si es necesario) es la memoria temporal que se usa internamente durante la ejecución del operador, por lo que no es necesario preocuparse por su contenido. No es necesario que lo mantenga una vez que se haya completado la llamada a [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) en la GPU. Esto significa que la aplicación puede liberar o sobrescribir el recurso temporal entre los envíos del operador compilado. El intervalo de búfer proporcionado que se va a enlazar como el recurso temporal debe estar alineado con el desplazamiento de inicio en [**DML_TEMPORARY_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). El tipo del montón subyacente del búfer debe ser **D3D12_HEAP_TYPE_DEFAULT**.

Sin embargo, si el distribuidor informa de un tamaño distinto de cero para su recurso persistente de larga duración, el procedimiento es ligeramente diferente. Debe crear un búfer y describir un enlace siguiendo el mismo patrón que se mostró anteriormente. Pero agréguelo a la tabla de enlace del inicializador del operador con una llamada a [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs), porque es el trabajo del inicializador del operador para inicializar el recurso persistente. A continuación, agréguelo a la tabla de enlace del operador compilada con una llamada a [**IDMLBindingTable:: BindPersistentResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource). Vea el ejemplo de código de la [aplicación DirectML mínima](dml-min-app.md) para ver este flujo de trabajo en acción. El contenido y la duración del recurso persistente deben persistir siempre que el operador compilado lo tenga. Es decir, si un operador requiere un recurso persistente, la aplicación debe proporcionarlo durante la inicialización y, a continuación, proporcionarlo también a todas las ejecuciones futuras del operador sin modificar su contenido. El recurso persistente normalmente lo usa DirectML para almacenar tablas de búsqueda u otros datos de larga duración que se calculan durante la inicialización de un operador y se reutilizan en futuras ejecuciones de ese operador. El intervalo de búfer proporcionado que se va a enlazar como búfer persistente debe estar alineado con el desplazamiento de inicio en [**DML_PERSISTENT_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). El tipo del montón subyacente del búfer debe ser **D3D12_HEAP_TYPE_DEFAULT**.

## <a name="describe-and-bind-any-tensors"></a>Describir y enlazar los diez

Si está tratando con un operador compilado (en lugar de con un inicializador de operador), debe enlazar los recursos de entrada y salida (para los de decenas y otros parámetros) a la tabla de enlace del operador. El número de enlaces debe coincidir exactamente con el número de entradas del operador, incluidos los de decenas opcionales. Los diez idiomas de entrada y salida determinados y otros parámetros que un operador toma se documentan en el tema correspondiente a ese operador (por ejemplo, [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)).

Un recurso tensores es un búfer que contiene los valores individuales de los elementos de tensores. Puede cargar y leer este tipo de búfer a/desde la GPU mediante las técnicas de Direct3D 12 normales ([cargar recursos](/windows/desktop/direct3d12/uploading-resources) y [leer datos a través de un búfer](/windows/desktop/direct3d12/readback-data-using-heaps)). Vea el ejemplo de código de la [aplicación DirectML mínima](dml-min-app.md) para ver estas técnicas en acción.

Por último, describa los enlaces de recursos de entrada y salida con estructuras **DML_BUFFER_BINDING** y **DML_BINDING_DESC** y, a continuación, agréguelos a la tabla de enlace del operador compilado con llamadas a [**IDMLBindingTable:: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) y [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs). Cuando se llama a un método **IDMLBindingTable: \* : Bind* _, DirectML escribe uno o más descriptores en el intervalo de descriptores de la CPU.

```cppwinrt
DML_BUFFER_BINDING inputBufferBinding{ inputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC inputBindingDesc{ DML_BINDING_TYPE_BUFFER, &inputBufferBinding };
dmlBindingTable->BindInputs(1, &inputBindingDesc);

DML_BUFFER_BINDING outputBufferBinding{ outputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC outputBindingDesc{ DML_BINDING_TYPE_BUFFER, &outputBufferBinding };
dmlBindingTable->BindOutputs(1, &outputBindingDesc);
```

Uno de los pasos para crear un operador DirectML (vea [_ *IDMLDevice:: CreateOperator* *](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator)) es declarar una o varias estructuras [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) para describir los búferes de datos tensores que el operador toma y devuelve. Además del tipo y el tamaño del búfer de tensores, puede especificar la marca de [**DML_TENSOR_FLAG_OWNED_BY_DML**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) opcionalmente.

**DML_TENSOR_FLAG_OWNED_BY_DML** indica que los datos de tensores deben ser propiedad y administrados por DirectML. DirectML realiza una copia de los datos de tensores durante la inicialización del operador y lo almacena en el recurso persistente. Esto permite a DirectML realizar el cambio de formato de los datos de tensores en formularios más eficaces. La configuración de esta marca puede aumentar el rendimiento, pero normalmente solo es útil para los que no cambian los datos durante la vigencia del operador (por ejemplo, los diez pesos). Y la marca solo se puede usar en los idiomas de entrada. Cuando la marca se establece en una descripción de tensores determinada, el tensores correspondiente debe estar enlazado a la tabla de enlace durante la inicialización del operador y no durante la ejecución (lo que producirá un error). Es lo contrario del comportamiento predeterminado (el comportamiento sin la marca de DML_TENSOR_FLAG_OWNED_BY_DML), donde se espera que el tensores esté enlazado durante la ejecución y no durante la inicialización. Cuando se proporcionan los datos de tensores a un inicializador de operador, es válido enlazar una carga en lugar de un montón predeterminado, ya que DirectML realiza una copia de los datos. En todos los demás casos, todos los recursos enlazados a DirectML deben ser recursos del montón predeterminados.

Para obtener más información, vea [**IDMLBindingTable:: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) y [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs).

## <a name="execute-the-dispatchable"></a>Ejecutar el distribuidor

Pase la tabla de enlace como un parámetro al llamar a [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

Cuando se usa la tabla de enlace durante una llamada a **IDMLCommandRecorder:: RecordDispatch**, DirectML enlaza los descriptores de GPU correspondientes a la canalización. No es necesario que los identificadores de descriptor de CPU y GPU señalen a las mismas entradas en un montón de descriptores; sin embargo, es responsabilidad de la aplicación asegurarse de que todo el intervalo de descriptor al que hace referencia el identificador de descriptor de CPU se copia en el intervalo al que hace referencia el identificador de descriptor de GPU antes de la ejecución

```cppwinrt
winrt::com_ptr<::ID3D12GraphicsCommandList> d3D12GraphicsCommandList;
// Code to create a Direct3D 12 command list goes here.

winrt::com_ptr<::IDMLCommandRecorder> dmlCommandRecorder;
// Code to create a DirectML command recorder goes here.

dmlCommandRecorder->RecordDispatch(
    d3D12GraphicsCommandList.get(),
    dmlOperatorInitializer.get(),
    dmlBindingTable.get()
);
```

Por último, cierre la lista de comandos de Direct3D 12 y envíelo para su ejecución como lo haría con cualquier otra lista de comandos.

Antes de la ejecución de **RecordDispatch** en la GPU, debe pasar todos los recursos enlazados al estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** , o a un estado que se pueda promover implícitamente a **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, como **D3D12_RESOURCE_STATE_COMMON**. Una vez finalizada esta llamada, los recursos permanecen en el estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . La única excepción a esto se debe a que los montones de carga están enlazados al ejecutar un inicializador de operador y mientras que uno o varios de los decenas tienen establecida la marca **DML_TENSOR_FLAG_OWNED_BY_DML** . En ese caso, los montones de carga enlazados a la entrada deben estar en el estado **D3D12_RESOURCE_STATE_GENERIC_READ** y permanecerán en ese estado, según lo requieran todos los montones de carga. Si no se estableció **DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE** al compilar el operador, se deben establecer todos los enlaces en la tabla de enlace antes de llamar a **RecordDispatch** , de lo contrario, el comportamiento es indefinido. De lo contrario, si un operador admite el [enlace en tiempo](#optionally-specify-late-bound-operator-bindings)de ejecución, se puede diferir el enlace de los recursos hasta que la lista de comandos de Direct3D 12 se envíe a la cola de comandos para su ejecución.

**RecordDispatch** actúa lógicamente como una llamada a [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch). Como tal, las barreras de la vista de acceso no ordenada (UAV) son necesarias para garantizar el orden correcto si hay dependencias de datos entre los envíos. Este método no inserta barreras UAV en los recursos de entrada ni de salida. La aplicación debe asegurarse de que se realicen las barreras UAV correctas en cualquier entrada si su contenido depende de una distribución ascendente, y en cualquier salida si hay envíos de nivel inferior que dependen de esas salidas.

## <a name="lifetime-and-synchronization-of-descriptors-and-binding-table"></a>Duración y sincronización de los descriptores y la tabla de enlace

Un buen modelo mental de enlace en DirectML es que, en segundo plano, la propia tabla de enlace DirectML es crear y administrar descriptores de vista de acceso no ordenado (UAV) dentro del montón de descriptores que se proporciona. Por lo tanto, todas las reglas habituales de Direct3D 12 se aplican en torno a la sincronización del acceso a ese montón y a sus descriptores. Es responsabilidad de la aplicación realizar una sincronización correcta entre el trabajo de CPU y GPU que usa una tabla de enlace.

Una tabla de enlace no puede sobrescribir un descriptor mientras el descriptor está en uso (por ejemplo, por un marco anterior). Por lo tanto, si desea volver a usar un montón de descriptor ya enlazado (por ejemplo, llamando a Bind * de nuevo en una tabla de enlace que apunte a él o sobrescribiendo el montón del descriptor manualmente), debe esperar a que el distribuidor que está utilizando actualmente el montón descriptor termine de ejecutarse en la GPU. Una tabla de enlace no mantiene una referencia fuerte en el montón de descriptores en el que escribe, por lo que no debe liberar el montón de descriptor visible del sombreador de copia de seguridad hasta que todo el trabajo que usa esa tabla de enlace haya completado la ejecución en la GPU.

Por otro lado, mientras que una tabla de enlace especifica y administra un montón de descriptores, la tabla no *contiene* ninguna de esa memoria. Por lo tanto, puede liberar o restablecer una tabla de enlace en cualquier momento después de haber llamado a [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) (no es necesario esperar a que la llamada se complete en la GPU, siempre y cuando los descriptores subyacentes sigan siendo válidos).

La tabla de enlace no mantiene referencias seguras en ningún recurso enlazado mediante la &mdash; aplicación debe asegurarse de que los recursos no se eliminen mientras la GPU los esté usando. Además, una tabla de enlace no es segura para subprocesos &mdash; la aplicación no debe llamar a métodos de una tabla de enlace simultáneamente desde distintos subprocesos sin sincronización.

Y tenga en cuenta que, en cualquier caso, el reenlace solo es necesario cuando se cambian los recursos que se enlazan. Si no necesita cambiar los recursos enlazados, puede enlazar una vez al inicio y pasar la misma tabla de enlace cada vez que llame a **RecordDispatch**.

Para intercalar las cargas de trabajo de representación y aprendizaje automático, solo tiene que asegurarse de que las tablas de enlace de cada fotograma apunten a los intervalos del montón del descriptor que ya no se usan en la GPU.

## <a name="optionally-specify-late-bound-operator-bindings"></a>Opcionalmente, especifique los enlaces de operador enlazados en tiempo de ejecución

Si está tratando con un operador compilado (en lugar de con un inicializador de operador), tiene la opción de especificar el enlace en tiempo de ejecución para el operador. Sin enlace en tiempo de ejecución, debe establecer todos los enlaces en la tabla de enlace antes de grabar un operador en una lista de comandos. Con el enlace en tiempo de ejecución, puede establecer (o cambiar) enlaces en operadores que ya ha grabado en una lista de comandos, antes de que se envíen a la cola de comandos.

Para especificar el enlace en tiempo de ejecución, llame a [**IDMLDevice:: CompileOperator**](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator) con un `flags` argumento de [**DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE**](/windows/desktop/api/directml/ne-directml-dml_execution_flags).