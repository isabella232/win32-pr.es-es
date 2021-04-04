---
title: oleautomation (atributo)
description: Compatibilidad y atributo oleautomation de MIDL con Automation.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- oleautomation (atributo) MIDL
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077733"
---
# <a name="oleautomation-attribute"></a>oleautomation (atributo)

El atributo **oleautomation** indica que una interfaz es compatible con la automatización.

``` syntax
[ 
    oleautomation, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
    ...
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*cadena: UUID* 
</dt> <dd>

Especifica una cadena de UUID generada por la utilidad Uuidgen.

</dd> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica otros atributos que se aplican a la interfaz en conjunto.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Especifica el nombre de una interfaz de automatización de la que esta interfaz derivada hereda las funciones miembro, los códigos de estado y los atributos de interfaz. Todas las interfaces de automatización se derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los parámetros y los tipos de valor devueltos especificados para los miembros de una interfaz **\[ oleautomation \]** deben ser compatibles con la automatización, como se muestra en la tabla siguiente.



| Tipo                                            | Descripción                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | Elemento de datos que puede tener el valor VARIANT \_ true o Variant \_ false. El tamaño corresponde a variante \_ bool.                                                                                                     |
| **unsigned char**                               | elemento de datos sin signo de 8 bits.                                                                                                                                                                                     |
| **double**                                      | número de punto flotante IEEE de 64 bits.                                                                                                                                                                            |
| **float**                                       | número de punto flotante IEEE de 32 bits.                                                                                                                                                                            |
| **int**                                         | Entero con signo, cuyo tamaño depende del sistema. En las plataformas de 32 bits, MIDL trata [**int**](int.md) como un entero con signo de 32 bits.                                                                               |
| **long**                                        | Entero con signo de 32 bits.                                                                                                                                                                                        |
| **short**                                       | entero de 16 bits con signo.                                                                                                                                                                                        |
| **UTILICEN**                                        | Cadena con prefijo de longitud, como se describe en el tema de automatización [BSTR](/previous-versions/windows/desktop/automat/bstr).                                                                                                    |
| **CURRENCY**                                    | número de punto flotante fijo de 8 bytes.                                                                                                                                                                          |
| **DATE**                                        | 64: número fraccionario de días de punto flotante desde el 30 de diciembre de 1899.                                                                                                                                     |
| **SCODE**                                       | Para sistemas de 16 bits: tipo de error integrado que corresponde a un error de VT \_ .                                                                                                                                         |
| **Typedef (enumeración** ) Â  *enum*                      | Entero con signo, cuyo tamaño depende del sistema.                                                                                                                                                               |
| **Interfaz IDispatch \***                      | Puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (distribución de VT \_ ).                                                                                                                |
| **Interfaz IUnknown \***                       | Puntero a una interfaz que no se deriva de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ Unknown). (Cualquier interfaz OLE se puede representar mediante su interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ). |
| **dispinterface**  *TypeName \**                | Puntero a una interfaz derivada de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (distribución de VT \_ ).                                                                                                    |
| **Coclase**  *TypeName \**                      | Puntero a un nombre de coclase (VT \_ desconocido).                                                                                                                                                                      |
| **\[ oleautomation ( \] interfaz**),  *TypeName \** | Puntero a una interfaz que se deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).                                                                                                                                      |
| **SAFEARRAY**(*TypeName*)                       | *TypeName* es cualquiera de los tipos anteriores. Matriz de estos tipos.                                                                                                                                                   |
| **NombreDeTipo \***                                 | *TypeName* es cualquiera de los tipos anteriores. Puntero a un tipo.                                                                                                                                                      |
| **Decimal**                                     | entero binario sin signo de 96 bits reducido por una potencia variable de 10. Un tipo de datos decimal que proporciona un tamaño y una escala para un número (como en coordenadas).                                                       |



 

Un parámetro es compatible con la automatización si su tipo es un tipo compatible con automatización, un puntero a un tipo compatible con automatización o una matriz SAFEARRAY de un tipo compatible con automatización.

Un tipo de valor devuelto es compatible con la automatización si su tipo es HRESULT, SCODE o [**void**](void.md). Sin embargo, MIDL requiere que los métodos de interfaz devuelvan HRESULT o SCODE. Si se devuelve **void** , se genera un error del compilador.

Un miembro es compatible con la automatización si su tipo de valor devuelto y todos sus parámetros son compatibles con la automatización.

Una interfaz es compatible con la automatización si se deriva de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) o [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), tiene el atributo **\[ oleautomation \]** y todas sus entradas VTBL son compatibles con la automatización. En el caso de las plataformas de 32 bits, la Convención de llamada para todos los métodos de la interfaz debe ser STDCALL. En los sistemas de 16 bits, todos los métodos deben tener la Convención de llamada CDECL.

Cada [**dispinterface**](dispinterface.md) es compatible implícitamente con la automatización. Por lo tanto, no debe usar el atributo **\[ \] oleautomation** en **dispinterface**.

El atributo **\[ \] oleautomation** no está disponible al compilar mediante el modificador [**/OSF**](-osf.md) del compilador MIDL.

### <a name="flags"></a>Marcas

TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>Ejemplos

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 