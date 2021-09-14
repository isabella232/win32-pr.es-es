---
title: oleautomation (atributo)
description: Atributo de oleautomación MIDL y compatibilidad con Automation.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- atributo oleautomation MIDL
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159439"
---
# <a name="oleautomation-attribute"></a>oleautomation (atributo)

El **atributo oleautomation** indica que una interfaz es compatible con Automation.

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

*string-uuid* 
</dt> <dd>

Especifica una cadena UUID generada por la utilidad Uuidgen.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica otros atributos que se aplican a la interfaz en su conjunto.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*interfaz base* 
</dt> <dd>

Especifica el nombre de una interfaz de Automation de la que esta interfaz derivada hereda funciones miembro, códigos de estado y atributos de interfaz. Todas las interfaces de Automation se derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**o IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los parámetros y los tipos de valor devuelto especificados para los miembros de una interfaz **\[ oleautomation \]** deben ser compatibles con Automation, como se muestra en la tabla siguiente.



| Tipo                                            | Descripción                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | Elemento de datos que puede tener el valor VARIANT \_ TRUE o VARIANT \_ FALSE. El tamaño corresponde a VARIANT \_ BOOL.                                                                                                     |
| **unsigned char**                               | Elemento de datos de 8 bits sin signo.                                                                                                                                                                                     |
| **double**                                      | Número de punto flotante IEEE de 64 bits.                                                                                                                                                                            |
| **float**                                       | Número de punto flotante IEEE de 32 bits.                                                                                                                                                                            |
| **int**                                         | Entero con signo, cuyo tamaño depende del sistema. En plataformas de 32 bits, MIDL trata [**int**](int.md) como un entero de 32 bits con signo.                                                                               |
| **long**                                        | Entero con signo de 32 bits.                                                                                                                                                                                        |
| **short**                                       | Entero de 16 bits con signo.                                                                                                                                                                                        |
| **BSTR**                                        | Cadena con prefijo de longitud, como se describe en el tema de Automation [BSTR](/previous-versions/windows/desktop/automat/bstr).                                                                                                    |
| **CURRENCY**                                    | Número fijo de punto flotante de 8 bytes.                                                                                                                                                                          |
| **DATE**                                        | Número fraccional de punto flotante de 64 bits desde el 30 de diciembre de 1899.                                                                                                                                     |
| **SCODE**                                       | Para sistemas de 16 bits: tipo de error integrado que corresponde a VT \_ ERROR.                                                                                                                                         |
| **Enumeración typedef** Â *myenum*                      | Entero con signo, cuyo tamaño depende del sistema.                                                                                                                                                               |
| **Interfaz IDispatch \** _                      | Puntero a la [interfaz _ *IDispatch* *](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ DISPATCH).                                                                                                                |
| **Interfaz IUnknown \** _                       | Puntero a una interfaz que no deriva de [_ *IDispatch* *](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ UNKNOWN). (Cualquier interfaz OLE se puede representar mediante su [**interfaz IUnknown).**](/windows/win32/api/unknwn/nn-unknwn-iunknown) |
| **dispinterface** Â *Typename \**                | Puntero a una interfaz derivada de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ DISPATCH).                                                                                                    |
| **Coclase** Â *Typename \**                      | Puntero a un nombre de la coclase (VT \_ UNKNOWN).                                                                                                                                                                      |
| **\[ oleautomation \] interface** Â *Typename \** | Puntero a una interfaz que deriva de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).                                                                                                                                      |
| **SAFEARRAY**(*TypeName*)                       | *TypeName* es cualquiera de los tipos anteriores. Matriz de estos tipos.                                                                                                                                                   |
| **TypeName \** _                                 | _TypeName* es cualquiera de los tipos anteriores. Puntero a un tipo.                                                                                                                                                      |
| **Decimal**                                     | Entero binario sin signo de 96 bits escalado por una potencia variable de 10. Tipo de datos decimal que proporciona un tamaño y una escala para un número (como en coordenadas).                                                       |



 

Un parámetro es compatible con Automation si su tipo es compatible con Automation, un puntero a un tipo compatible con Automation o un SAFEARRAY de un tipo compatible con Automation.

Un tipo de valor devuelto es compatible con Automation si su tipo es HRESULT, SCODE o [**void.**](void.md) Sin embargo, MIDL requiere que los métodos de interfaz devuelvan HRESULT o SCODE. La **devolución de void** genera un error del compilador.

Un miembro es compatible con Automation si su tipo de valor devuelto y todos sus parámetros son compatibles con Automation.

Una interfaz es compatible con Automation si se deriva de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) o [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)tiene el atributo **\[ oleautomation \]** y todas sus entradas VTBL son compatibles con Automation. Para las plataformas de 32 bits, la convención de llamada para todos los métodos de la interfaz debe ser STDCALL. Para los sistemas de 16 bits, todos los métodos deben tener la convención de llamada CDECL.

Cada [**dispinterface**](dispinterface.md) es implícitamente compatible con Automation. Por lo tanto, no debe usar **\[ el atributo oleautomation \]** en **dispinterface**.

El **\[ atributo oleautomation \]** no está disponible cuando se compila mediante el modificador [**/osf del**](-osf.md) compilador de MIDL.

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

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 